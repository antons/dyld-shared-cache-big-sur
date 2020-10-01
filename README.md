Modifications to Apple's dyld project to fix Objective-C information when extracting dyld_shared_cache from macOS Big Sur to help Hopper generate readable pseudocode.

Note: macOS Big Sur beta 9 changed the format of dyld_shared_cache. Currently this project only supports beta 1-8.

### Usage

1. Build `dyld_shared_cache_util` sheme, which will also build its dependency `dsc_extractor`. `dyld_shared_cache_util` is modified to look for `dsc_extractor` in the same directory.
2. `./dyld_shared_cache_util -extract ~/Developer/macOS\ Big\ Sur /System/Library/dyld/dyld_shared_cache_x86_64`.
3. Decompile the extracted libraries with Hopper.
