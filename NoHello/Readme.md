# NoHello
NoHello is a KPM used to hide various root detection developed by @MhmRdd

This KPM should support Kernels from 4.4 to 6.12+

Follow him and Support him in GitHub Here: https://github.com/MhmRdd

KPMs are normally released in his Telegram channel: https://t.me/welikeandroid

All Rights belong to the original developer! I'm just keeping this for my personal use or quick indexing and sharing. 

# Changelogs

## Nohello-v1.8.2.9-80-35888e6-release.kpm
- Do not restrict kpm when kernel version is not supporting unicode/ext4
- Added resolution of 'kallsyms_lookup_size_offset'
- Guard the patch against overflow of table size.

## Nohello-v1.8.2.9-79-dd44e4e-release.kpm
- Added unicode patch: "Don't use case ignorable code points". (CVE-2024-43093)
NOTE: This patch takes effect only when embedding KPM, it's not possible to patch the kernel live when unicode mappings are being populated.

## Nohello-v1.8.2.9-77-4dc2fa2-release.kpm
- Added alternative for finding PAGE_SHIFT/PAGE_SZ in kernel (tcr_el1 & tg1).

## Nohello-v1.8.2.9-76-4cab50e-release.kpm
- Fix kernels 4.14.x/4.4.x compatibility issue, use _text and fallback to _stext when not found.
- Fix mistake when looking in fallback for analysing mmap_write_lock_killable/mmap_write_unlock directly (affects kernels 6.12.x+)

## Nohello-v1.8.2.9-72-7ec38ce-release.kpm
- Fix compat with KernelPatch 0.12.4 (from now on, supports only 0.12.4+)
- Thanks to @ ec_curve for making sure it's only 0.12.4+

## Nohello-v1.8.2.9-71-796a067-release.kpm
- Fix an issue with resolving instruction(s) 'cas' for arm64
- Fix submodule arm64_vartracker to handle 'cas' instructions correctly.
- 'mmap_lock' is taken now within first order of occurence from vartracker (no checks are done).

## Nohello-v1.8.2.9-70-b7c5677-release.kpm
- Fix an issue with resolving instruction(s) 'casa' for arm64
- Fix submodule cfg to use code buffer not direct address
- Added verbosing for vartracking (future failings should be resolved by kernel messages provided by the user).
- Added return policy for finding current->mm & mm->mmap_lock
