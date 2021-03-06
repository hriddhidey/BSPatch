# BSPatch

![GitHub release](https://img.shields.io/github/release/hriddhidey/BSPatch.svg?style=for-the-badge)
![License](https://img.shields.io/cocoapods/l/BSPatch.svg?style=for-the-badge)
![Platform](https://img.shields.io/cocoapods/p/BSPatch.svg?style=for-the-badge)

BSPatch is a cocoapod library that implements the popular `bspatch` utility as detailed by Colin Percival [here](http://www.daemonology.net/bsdiff/). It will apply a patchfile generated by the `bsdiff` binary diffing utility onto a base file, to generate the outfile that would've been used as the target to generate the diff.

## Requirements

Requires only XCode, and CocoaPods.

## Installation

BSPatch is not available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile, to reference it from this repo:

```ruby
pod 'BSPatch', :git => 'https://github.com/hriddhidey/BSPatch.git', :branch => '0.6.0'
```

## Usage

Simply import the library and call the `bspatch()` function.
```
#import <BSPatch/BSPatch.h>

...
...

const char *oldFile = // path to your original file
const char *newFile = // path to your new file - does not need to exist, file will be created if not found.
const char *patchfile = // patch to your patch file
int res = bspatch(oldFile, newFile, patchfile);
// Returns 0 if successful
if (res != 0) {
  NSLog(@"Error while patching file. Error status: %@", [@(res) stringValue]);
  return;
}
```

## License

BSPatch is available under the MIT license.
