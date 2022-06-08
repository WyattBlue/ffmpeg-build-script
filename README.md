build-ffmpeg
==========

## Usage

```bash
Usage: build-ffmpeg [OPTIONS]
Options:
  -h, --help                     Display usage information
      --version                  Display version information
  -b, --build                    Starts the build process
      --enable-gpl-and-non-free  Enable non-free codecs  - https://ffmpeg.org/legal.html
      --latest                   Build latest version of dependencies if newer available
  -c, --cleanup                  Remove all working dirs
      --full-static              Complete static build of ffmpeg (eg. glibc, pthreads etc...) **only Linux**
                                 Note: Because of the NSS (Name Service Switch), glibc does not recommend static links.
```

## Notes of static link

- Because of the NSS (Name Service Switch), glibc does **not recommend** static links. See detail
  below: https://sourceware.org/glibc/wiki/FAQ#Even_statically_linked_programs_need_some_shared_libraries_which_is_not_acceptable_for_me.__What_can_I_do.3F

- The libnpp in the CUDA SDK cannot be statically linked.
- Vaapi cannot be statically linked.

