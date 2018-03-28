# BSPatch

[![CI Status](http://img.shields.io/travis/hriddhidey@gmail.com/BSPatch.svg?style=flat)](https://travis-ci.org/hriddhidey@gmail.com/BSPatch)
[![Version](https://img.shields.io/cocoapods/v/BSPatch.svg?style=flat)](http://cocoapods.org/pods/BSPatch)
[![License](https://img.shields.io/cocoapods/l/BSPatch.svg?style=flat)](http://cocoapods.org/pods/BSPatch)
[![Platform](https://img.shields.io/cocoapods/p/BSPatch.svg?style=flat)](http://cocoapods.org/pods/BSPatch)

## Requirements

Requires only XCode, and CocoaPods.

## Installation

BSPatch is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod 'BSPatch'
```

Or, reference is from this repository and set the branch to the latest release tag.

## Usage

Simply import the library and call the `bspatch()` function.
```
#import <BSPatch/BSPatch.h>

...
...

const char *oldFile = // path to your original file
const char *newFile = // path to your new file
const char *patchfile = // patch to your patch file
int res = bspatch(oldFile, newFile, patchfile);
// Returns 0 if successful
if (res != 0) {
  NSLog(@"Error while patching file. Error status: %@", [@(res) stringValue]);
  return;
}
```

## License

BSPatch is available under the MIT license. See the LICENSE file for more info.
