# api documentation for  [mock-fs (v4.2.0)](https://github.com/tschaub/mock-fs)  [![npm package](https://img.shields.io/npm/v/npmdoc-mock-fs.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-mock-fs) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-mock-fs.svg)](https://travis-ci.org/npmdoc/node-npmdoc-mock-fs)
#### A configurable mock file system.  You know, for testing.

[![NPM](https://nodei.co/npm/mock-fs.png?downloads=true)](https://www.npmjs.com/package/mock-fs)

[![apidoc](https://npmdoc.github.io/node-npmdoc-mock-fs/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-mock-fs_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-mock-fs/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-mock-fs/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-mock-fs/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Tim Schaub",
        "url": "http://tschaub.net/"
    },
    "bugs": {
        "url": "https://github.com/tschaub/mock-fs/issues"
    },
    "dependencies": {},
    "description": "A configurable mock file system.  You know, for testing.",
    "devDependencies": {
        "bench-it": "0.4.0",
        "chai": "3.5.0",
        "eslint": "^3.11.1",
        "eslint-config-tschaub": "^6.0.0",
        "mocha": "3.1.2",
        "rimraf": "2.5.4"
    },
    "directories": {},
    "dist": {
        "shasum": "ef53ae17b77e64f67816dd0467f29208a3b26e19",
        "tarball": "https://registry.npmjs.org/mock-fs/-/mock-fs-4.2.0.tgz"
    },
    "gitHead": "d7532caa28638a01784921e6f980cf8b79f3d54e",
    "homepage": "https://github.com/tschaub/mock-fs",
    "keywords": [
        "mock",
        "fs",
        "test",
        "fixtures",
        "file system",
        "memory"
    ],
    "license": "MIT",
    "main": "lib/index.js",
    "maintainers": [
        {
            "name": "tschaub",
            "email": "tim.schaub@gmail.com"
        }
    ],
    "name": "mock-fs",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/tschaub/mock-fs.git"
    },
    "scripts": {
        "bench": "bench benchmarks",
        "pretest": "eslint benchmarks lib test",
        "test": "mocha --recursive test"
    },
    "version": "4.2.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module mock-fs](#apidoc.module.mock-fs)
1.  [function <span class="apidocSignatureSpan">mock-fs.</span>binding (system)](#apidoc.element.mock-fs.binding)
1.  [function <span class="apidocSignatureSpan">mock-fs.</span>descriptor (flags)](#apidoc.element.mock-fs.descriptor)
1.  [function <span class="apidocSignatureSpan">mock-fs.</span>directory (config)](#apidoc.element.mock-fs.directory)
1.  [function <span class="apidocSignatureSpan">mock-fs.</span>file (config)](#apidoc.element.mock-fs.file)
1.  [function <span class="apidocSignatureSpan">mock-fs.</span>filesystem (options)](#apidoc.element.mock-fs.filesystem)
1.  [function <span class="apidocSignatureSpan">mock-fs.</span>getMockRoot ()](#apidoc.element.mock-fs.getMockRoot)
1.  [function <span class="apidocSignatureSpan">mock-fs.</span>item ()](#apidoc.element.mock-fs.item)
1.  [function <span class="apidocSignatureSpan">mock-fs.</span>restore ()](#apidoc.element.mock-fs.restore)
1.  [function <span class="apidocSignatureSpan">mock-fs.</span>symlink (config)](#apidoc.element.mock-fs.symlink)
1.  object <span class="apidocSignatureSpan">mock-fs.</span>binding.prototype
1.  object <span class="apidocSignatureSpan">mock-fs.</span>descriptor.prototype
1.  object <span class="apidocSignatureSpan">mock-fs.</span>directory.prototype
1.  object <span class="apidocSignatureSpan">mock-fs.</span>file.prototype
1.  object <span class="apidocSignatureSpan">mock-fs.</span>filesystem.prototype
1.  object <span class="apidocSignatureSpan">mock-fs.</span>item.prototype
1.  object <span class="apidocSignatureSpan">mock-fs.</span>symlink.prototype

#### [module mock-fs.binding](#apidoc.module.mock-fs.binding)
1.  [function <span class="apidocSignatureSpan">mock-fs.</span>binding (system)](#apidoc.element.mock-fs.binding.binding)

#### [module mock-fs.binding.prototype](#apidoc.module.mock-fs.binding.prototype)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>StatWatcher ()](#apidoc.element.mock-fs.binding.prototype.StatWatcher)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>_getDescriptorById (fd)](#apidoc.element.mock-fs.binding.prototype._getDescriptorById)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>_trackDescriptor (descriptor)](#apidoc.element.mock-fs.binding.prototype._trackDescriptor)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>_untrackDescriptorById (fd)](#apidoc.element.mock-fs.binding.prototype._untrackDescriptorById)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>access (filepath, mode, callback)](#apidoc.element.mock-fs.binding.prototype.access)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>chmod (pathname, mode, callback)](#apidoc.element.mock-fs.binding.prototype.chmod)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>chown (pathname, uid, gid, callback)](#apidoc.element.mock-fs.binding.prototype.chown)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>close (fd, callback)](#apidoc.element.mock-fs.binding.prototype.close)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>fchmod (fd, mode, callback)](#apidoc.element.mock-fs.binding.prototype.fchmod)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>fchown (fd, uid, gid, callback)](#apidoc.element.mock-fs.binding.prototype.fchown)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>fdatasync (fd, callback)](#apidoc.element.mock-fs.binding.prototype.fdatasync)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>fstat (fd, callback)](#apidoc.element.mock-fs.binding.prototype.fstat)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>fsync (fd, callback)](#apidoc.element.mock-fs.binding.prototype.fsync)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>ftruncate (fd, len, callback)](#apidoc.element.mock-fs.binding.prototype.ftruncate)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>futimes (fd, atime, mtime, callback)](#apidoc.element.mock-fs.binding.prototype.futimes)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>getSystem ()](#apidoc.element.mock-fs.binding.prototype.getSystem)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>link (srcPath, destPath, callback)](#apidoc.element.mock-fs.binding.prototype.link)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>lstat (filepath, callback)](#apidoc.element.mock-fs.binding.prototype.lstat)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>mkdir (pathname, mode, callback)](#apidoc.element.mock-fs.binding.prototype.mkdir)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>open (pathname, flags, mode, callback)](#apidoc.element.mock-fs.binding.prototype.open)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>read (fd, buffer, offset, length, position, callback)](#apidoc.element.mock-fs.binding.prototype.read)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>readdir (dirpath, encoding, callback)](#apidoc.element.mock-fs.binding.prototype.readdir)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>readlink (pathname, encoding, callback)](#apidoc.element.mock-fs.binding.prototype.readlink)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>realpath (filepath, encoding, callback)](#apidoc.element.mock-fs.binding.prototype.realpath)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>rename (oldPath, newPath, callback)](#apidoc.element.mock-fs.binding.prototype.rename)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>rmdir (pathname, callback)](#apidoc.element.mock-fs.binding.prototype.rmdir)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>setSystem (system)](#apidoc.element.mock-fs.binding.prototype.setSystem)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>stat (filepath, callback)](#apidoc.element.mock-fs.binding.prototype.stat)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>symlink (srcPath, destPath, type, callback)](#apidoc.element.mock-fs.binding.prototype.symlink)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>truncate (fd, len, callback)](#apidoc.element.mock-fs.binding.prototype.truncate)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>unlink (pathname, callback)](#apidoc.element.mock-fs.binding.prototype.unlink)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>utimes (pathname, atime, mtime, callback)](#apidoc.element.mock-fs.binding.prototype.utimes)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>write (fd, buffer, offset, length, position, callback)](#apidoc.element.mock-fs.binding.prototype.write)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>writeBuffer (fd, buffer, offset, length, position, callback)](#apidoc.element.mock-fs.binding.prototype.writeBuffer)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>writeBuffers (fd, buffers, position, callback)](#apidoc.element.mock-fs.binding.prototype.writeBuffers)
1.  [function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>writeString (fd, string, position, encoding, callback)](#apidoc.element.mock-fs.binding.prototype.writeString)

#### [module mock-fs.descriptor](#apidoc.module.mock-fs.descriptor)
1.  [function <span class="apidocSignatureSpan">mock-fs.</span>descriptor (flags)](#apidoc.element.mock-fs.descriptor.descriptor)

#### [module mock-fs.descriptor.prototype](#apidoc.module.mock-fs.descriptor.prototype)
1.  [function <span class="apidocSignatureSpan">mock-fs.descriptor.prototype.</span>getItem ()](#apidoc.element.mock-fs.descriptor.prototype.getItem)
1.  [function <span class="apidocSignatureSpan">mock-fs.descriptor.prototype.</span>getPosition ()](#apidoc.element.mock-fs.descriptor.prototype.getPosition)
1.  [function <span class="apidocSignatureSpan">mock-fs.descriptor.prototype.</span>isAppend ()](#apidoc.element.mock-fs.descriptor.prototype.isAppend)
1.  [function <span class="apidocSignatureSpan">mock-fs.descriptor.prototype.</span>isCreate ()](#apidoc.element.mock-fs.descriptor.prototype.isCreate)
1.  [function <span class="apidocSignatureSpan">mock-fs.descriptor.prototype.</span>isExclusive ()](#apidoc.element.mock-fs.descriptor.prototype.isExclusive)
1.  [function <span class="apidocSignatureSpan">mock-fs.descriptor.prototype.</span>isRead ()](#apidoc.element.mock-fs.descriptor.prototype.isRead)
1.  [function <span class="apidocSignatureSpan">mock-fs.descriptor.prototype.</span>isTruncate ()](#apidoc.element.mock-fs.descriptor.prototype.isTruncate)
1.  [function <span class="apidocSignatureSpan">mock-fs.descriptor.prototype.</span>isWrite ()](#apidoc.element.mock-fs.descriptor.prototype.isWrite)
1.  [function <span class="apidocSignatureSpan">mock-fs.descriptor.prototype.</span>setItem (item)](#apidoc.element.mock-fs.descriptor.prototype.setItem)
1.  [function <span class="apidocSignatureSpan">mock-fs.descriptor.prototype.</span>setPosition (position)](#apidoc.element.mock-fs.descriptor.prototype.setPosition)

#### [module mock-fs.directory](#apidoc.module.mock-fs.directory)
1.  [function <span class="apidocSignatureSpan">mock-fs.</span>directory ()](#apidoc.element.mock-fs.directory.directory)
1.  [function <span class="apidocSignatureSpan">mock-fs.directory.</span>super_ ()](#apidoc.element.mock-fs.directory.super_)

#### [module mock-fs.directory.prototype](#apidoc.module.mock-fs.directory.prototype)
1.  [function <span class="apidocSignatureSpan">mock-fs.directory.prototype.</span>addItem (name, item)](#apidoc.element.mock-fs.directory.prototype.addItem)
1.  [function <span class="apidocSignatureSpan">mock-fs.directory.prototype.</span>getItem (name)](#apidoc.element.mock-fs.directory.prototype.getItem)
1.  [function <span class="apidocSignatureSpan">mock-fs.directory.prototype.</span>getStats ()](#apidoc.element.mock-fs.directory.prototype.getStats)
1.  [function <span class="apidocSignatureSpan">mock-fs.directory.prototype.</span>list ()](#apidoc.element.mock-fs.directory.prototype.list)
1.  [function <span class="apidocSignatureSpan">mock-fs.directory.prototype.</span>removeItem (name)](#apidoc.element.mock-fs.directory.prototype.removeItem)

#### [module mock-fs.file](#apidoc.module.mock-fs.file)
1.  [function <span class="apidocSignatureSpan">mock-fs.</span>file ()](#apidoc.element.mock-fs.file.file)
1.  [function <span class="apidocSignatureSpan">mock-fs.file.</span>super_ ()](#apidoc.element.mock-fs.file.super_)

#### [module mock-fs.file.prototype](#apidoc.module.mock-fs.file.prototype)
1.  [function <span class="apidocSignatureSpan">mock-fs.file.prototype.</span>getContent ()](#apidoc.element.mock-fs.file.prototype.getContent)
1.  [function <span class="apidocSignatureSpan">mock-fs.file.prototype.</span>getStats ()](#apidoc.element.mock-fs.file.prototype.getStats)
1.  [function <span class="apidocSignatureSpan">mock-fs.file.prototype.</span>setContent (content)](#apidoc.element.mock-fs.file.prototype.setContent)

#### [module mock-fs.filesystem](#apidoc.module.mock-fs.filesystem)
1.  [function <span class="apidocSignatureSpan">mock-fs.</span>filesystem (options)](#apidoc.element.mock-fs.filesystem.filesystem)
1.  [function <span class="apidocSignatureSpan">mock-fs.filesystem.</span>create (paths, options)](#apidoc.element.mock-fs.filesystem.create)
1.  [function <span class="apidocSignatureSpan">mock-fs.filesystem.</span>directory (config)](#apidoc.element.mock-fs.filesystem.directory)
1.  [function <span class="apidocSignatureSpan">mock-fs.filesystem.</span>file (config)](#apidoc.element.mock-fs.filesystem.file)
1.  [function <span class="apidocSignatureSpan">mock-fs.filesystem.</span>getPathParts (filepath)](#apidoc.element.mock-fs.filesystem.getPathParts)
1.  [function <span class="apidocSignatureSpan">mock-fs.filesystem.</span>symlink (config)](#apidoc.element.mock-fs.filesystem.symlink)

#### [module mock-fs.filesystem.prototype](#apidoc.module.mock-fs.filesystem.prototype)
1.  [function <span class="apidocSignatureSpan">mock-fs.filesystem.prototype.</span>getItem (filepath)](#apidoc.element.mock-fs.filesystem.prototype.getItem)
1.  [function <span class="apidocSignatureSpan">mock-fs.filesystem.prototype.</span>getRoot ()](#apidoc.element.mock-fs.filesystem.prototype.getRoot)

#### [module mock-fs.item](#apidoc.module.mock-fs.item)
1.  [function <span class="apidocSignatureSpan">mock-fs.</span>item ()](#apidoc.element.mock-fs.item.item)

#### [module mock-fs.item.prototype](#apidoc.module.mock-fs.item.prototype)
1.  [function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>canExecute ()](#apidoc.element.mock-fs.item.prototype.canExecute)
1.  [function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>canRead ()](#apidoc.element.mock-fs.item.prototype.canRead)
1.  [function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>canWrite ()](#apidoc.element.mock-fs.item.prototype.canWrite)
1.  [function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>getATime ()](#apidoc.element.mock-fs.item.prototype.getATime)
1.  [function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>getBirthtime ()](#apidoc.element.mock-fs.item.prototype.getBirthtime)
1.  [function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>getCTime ()](#apidoc.element.mock-fs.item.prototype.getCTime)
1.  [function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>getGid ()](#apidoc.element.mock-fs.item.prototype.getGid)
1.  [function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>getMTime ()](#apidoc.element.mock-fs.item.prototype.getMTime)
1.  [function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>getMode ()](#apidoc.element.mock-fs.item.prototype.getMode)
1.  [function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>getStats ()](#apidoc.element.mock-fs.item.prototype.getStats)
1.  [function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>getUid ()](#apidoc.element.mock-fs.item.prototype.getUid)
1.  [function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>setATime (atime)](#apidoc.element.mock-fs.item.prototype.setATime)
1.  [function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>setBirthtime (birthtime)](#apidoc.element.mock-fs.item.prototype.setBirthtime)
1.  [function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>setCTime (ctime)](#apidoc.element.mock-fs.item.prototype.setCTime)
1.  [function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>setGid (gid)](#apidoc.element.mock-fs.item.prototype.setGid)
1.  [function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>setMTime (mtime)](#apidoc.element.mock-fs.item.prototype.setMTime)
1.  [function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>setMode (mode)](#apidoc.element.mock-fs.item.prototype.setMode)
1.  [function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>setUid (uid)](#apidoc.element.mock-fs.item.prototype.setUid)
1.  [function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>toString ()](#apidoc.element.mock-fs.item.prototype.toString)

#### [module mock-fs.symlink](#apidoc.module.mock-fs.symlink)
1.  [function <span class="apidocSignatureSpan">mock-fs.</span>symlink ()](#apidoc.element.mock-fs.symlink.symlink)
1.  [function <span class="apidocSignatureSpan">mock-fs.symlink.</span>super_ ()](#apidoc.element.mock-fs.symlink.super_)

#### [module mock-fs.symlink.prototype](#apidoc.module.mock-fs.symlink.prototype)
1.  [function <span class="apidocSignatureSpan">mock-fs.symlink.prototype.</span>getPath ()](#apidoc.element.mock-fs.symlink.prototype.getPath)
1.  [function <span class="apidocSignatureSpan">mock-fs.symlink.prototype.</span>getStats ()](#apidoc.element.mock-fs.symlink.prototype.getStats)
1.  [function <span class="apidocSignatureSpan">mock-fs.symlink.prototype.</span>setPath (pathname)](#apidoc.element.mock-fs.symlink.prototype.setPath)



# <a name="apidoc.module.mock-fs"></a>[module mock-fs](#apidoc.module.mock-fs)

#### <a name="apidoc.element.mock-fs.binding"></a>[function <span class="apidocSignatureSpan">mock-fs.</span>binding (system)](#apidoc.element.mock-fs.binding)
- description and source-code
```javascript
function Binding(system) {

<span class="apidocCodeCommentSpan">  /**
   * Mock file system.
   * @type {FileSystem}
   */
</span>  this._system = system;

  /**
   * Stats constructor.
   * @type {function}
   */
  this.Stats = Stats;

  /**
   * Lookup of open files.
   * @type {Object.<number, FileDescriptor>}
   */
  this._openFiles = {};

  /**
   * Counter for file descriptors.
   * @type {number}
   */
  this._counter = 0;

}
```
- example usage
```shell
...
'''js
// after a test runs
mock.restore();
'''

## Upgrading to version 4

Instead of overriding all methods of the built-in 'fs' module, the library now overrides 'process.binding('fs')'.  The purpose of
 this change is to avoid conflicts with other libraries that override 'fs' methods (e.g. 'graceful-fs') and to make it possible
to work with multiple Node releases without maintaining copied and slightly modified versions of Node's 'fs' module.

Breaking changes:

* The 'mock.fs()' function has been removed.  This returned an object with 'fs'-like methods without overriding the built-in 'fs
' module.
* The object created by 'fs.Stats' is no longer an instance of 'fs.Stats' (though it has all the same properties and methods).
* Lazy 'require()' do not use the real filesystem.
* Tests are no longer run in Node < 4.
...
```

#### <a name="apidoc.element.mock-fs.descriptor"></a>[function <span class="apidocSignatureSpan">mock-fs.</span>descriptor (flags)](#apidoc.element.mock-fs.descriptor)
- description and source-code
```javascript
function FileDescriptor(flags) {

<span class="apidocCodeCommentSpan">  /**
   * Flags.
   * @type {number}
   */
</span>  this._flags = flags;

  /**
   * File system item.
   * @type {Item}
   */
  this._item = null;

  /**
   * Current file position.
   * @type {number}
   */
  this._position = 0;

}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.directory"></a>[function <span class="apidocSignatureSpan">mock-fs.</span>directory (config)](#apidoc.element.mock-fs.directory)
- description and source-code
```javascript
directory = function (config) {
  config = config || {};
  return function() {
    var dir = new Directory();
    if (config.hasOwnProperty('mode')) {
      dir.setMode(config.mode);
    }
    if (config.hasOwnProperty('uid')) {
      dir.setUid(config.uid);
    }
    if (config.hasOwnProperty('gid')) {
      dir.setGid(config.gid);
    }
    if (config.hasOwnProperty('items')) {
      for (var name in config.items) {
        populate(dir, name, config.items[name]);
      }
    }
    if (config.hasOwnProperty('atime')) {
      dir.setATime(config.atime);
    }
    if (config.hasOwnProperty('ctime')) {
      dir.setCTime(config.ctime);
    }
    if (config.hasOwnProperty('mtime')) {
      dir.setMTime(config.mtime);
    }
    if (config.hasOwnProperty('birthtime')) {
      dir.setBirthtime(config.birthtime);
    }
    return dir;
  };
}
```
- example usage
```shell
...
       file2: new Buffer([1, 2, 3, 4])
     }
   }
 }
});
'''

To create a directory with additional properties (owner, permissions, atime, etc.), use the ['mock.directory()'](mockdirectoryproperties
) function described below.

### <a id='mockdirectoryproperties'>'mock.directory(properties)'</a>

Create a factory for new directories.  Supported properties:

* **mode** - 'number' Directory mode (permission and sticky bits).  Defaults to '0777'.
* **uid** - 'number' The user id.  Defaults to 'process.getuid()'.
...
```

#### <a name="apidoc.element.mock-fs.file"></a>[function <span class="apidocSignatureSpan">mock-fs.</span>file (config)](#apidoc.element.mock-fs.file)
- description and source-code
```javascript
file = function (config) {
  config = config || {};
  return function() {
    var file = new File();
    if (config.hasOwnProperty('content')) {
      file.setContent(config.content);
    }
    if (config.hasOwnProperty('mode')) {
      file.setMode(config.mode);
    } else {
      file.setMode(438); // 0666
    }
    if (config.hasOwnProperty('uid')) {
      file.setUid(config.uid);
    }
    if (config.hasOwnProperty('gid')) {
      file.setGid(config.gid);
    }
    if (config.hasOwnProperty('atime')) {
      file.setATime(config.atime);
    }
    if (config.hasOwnProperty('ctime')) {
      file.setCTime(config.ctime);
    }
    if (config.hasOwnProperty('mtime')) {
      file.setMTime(config.mtime);
    }
    if (config.hasOwnProperty('birthtime')) {
      file.setBirthtime(config.birthtime);
    }
    return file;
  };
}
```
- example usage
```shell
...
When 'config' property values are a 'string' or 'Buffer', a file is created with the provided content.  For example, the following
 configuration creates a single file with string content (in addition to the two default directories).
'''js
mock({
 'path/to/file.txt': 'file content here'
});
'''

To create a file with additional properties (owner, permissions, atime, etc.), use the ['mock.file()'](#mockfileproperties) function
 described below.

### <a id='mockfileproperties'>'mock.file(properties)'</a>

Create a factory for new files.  Supported properties:

* **content** - 'string|Buffer' File contents.
* **mode** - 'number' File mode (permission and sticky bits).  Defaults to '0666'.
...
```

#### <a name="apidoc.element.mock-fs.filesystem"></a>[function <span class="apidocSignatureSpan">mock-fs.</span>filesystem (options)](#apidoc.element.mock-fs.filesystem)
- description and source-code
```javascript
function FileSystem(options) {
  options = options || {};

  var createCwd = 'createCwd' in options ? options.createCwd : true;
  var createTmp = 'createTmp' in options ? options.createTmp : true;

  var root = new Directory();

  // populate with default directories
  var defaults = [];
  if (createCwd) {
    defaults.push(process.cwd());
  }

  if (createTmp) {
    defaults.push(os.tmpdir && os.tmpdir() || os.tmpDir());
  }

  defaults.forEach(function(dir) {
    var parts = getPathParts(dir);
    var directory = root;
    var i, ii, name, candidate;
    for (i = 0, ii = parts.length; i < ii; ++i) {
      name = parts[i];
      candidate = directory.getItem(name);
      if (!candidate) {
        directory = directory.addItem(name, new Directory());
      } else if (candidate instanceof Directory) {
        directory = candidate;
      } else {
        throw new Error('Failed to create directory: ' + dir);
      }
    }
  });

<span class="apidocCodeCommentSpan">  /**
   * Root directory.
   * @type {Directory}
   */
</span>  this._root = root;

}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.getMockRoot"></a>[function <span class="apidocSignatureSpan">mock-fs.</span>getMockRoot ()](#apidoc.element.mock-fs.getMockRoot)
- description and source-code
```javascript
getMockRoot = function () {
  if (typeof realBinding.getSystem === 'undefined') {
    return {};
  } else {
    return realBinding.getSystem().getRoot();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.item"></a>[function <span class="apidocSignatureSpan">mock-fs.</span>item ()](#apidoc.element.mock-fs.item)
- description and source-code
```javascript
function Item() {

  var now = Date.now();

<span class="apidocCodeCommentSpan">  /**
   * Access time.
   * @type {Date}
   */
</span>  this._atime = new Date(now);

  /**
   * Change time.
   * @type {Date}
   */
  this._ctime = new Date(now);

  /**
   * Birth time.
   * @type {Date}
   */
  this._birthtime = new Date(now);

  /**
   * Modification time.
   * @type {Date}
   */
  this._mtime = new Date(now);

  /**
   * Permissions.
   */
  this._mode = 438; // 0666

  /**
   * User id.
   * @type {number}
   */
  this._uid = getUid();

  /**
   * Group id.
   * @type {number}
   */
  this._gid = getGid();

  /**
   * Item number.
   * @type {number}
   */
  this._id = ++counter;

  /**
   * Number of links to this item.
   */
  this.links = 0;

}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.restore"></a>[function <span class="apidocSignatureSpan">mock-fs.</span>restore ()](#apidoc.element.mock-fs.restore)
- description and source-code
```javascript
restore = function () {
  restoreBinding();
  restoreProcess();
}
```
- example usage
```shell
...
    'empty-dir': {/** empty directory */}
  },
  'path/to/some.png': new Buffer([8, 6, 7, 5, 3, 0, 9]),
  'some/other/path': {/** another empty directory */}
});
'''

When you are ready to restore the 'fs' module (so that it is backed by your real file system), call ['mock.restore()'](#mockrestore
). Note that calling this may be **mandatory** in some cases. See [istanbuljs/nyc#324](https://github.com/istanbuljs/nyc/issues/
324#issuecomment-234018654)

'''js
// after a test runs
mock.restore();
'''

## Upgrading to version 4
...
```

#### <a name="apidoc.element.mock-fs.symlink"></a>[function <span class="apidocSignatureSpan">mock-fs.</span>symlink (config)](#apidoc.element.mock-fs.symlink)
- description and source-code
```javascript
symlink = function (config) {
  config = config || {};
  return function() {
    var link = new SymbolicLink();
    if (config.hasOwnProperty('mode')) {
      link.setMode(config.mode);
    } else {
      link.setMode(438); // 0666
    }
    if (config.hasOwnProperty('uid')) {
      link.setUid(config.uid);
    }
    if (config.hasOwnProperty('gid')) {
      link.setGid(config.gid);
    }
    if (config.hasOwnProperty('path')) {
      link.setPath(config.path);
    } else {
      throw new Error('Missing "path" property');
    }
    if (config.hasOwnProperty('atime')) {
      link.setATime(config.atime);
    }
    if (config.hasOwnProperty('ctime')) {
      link.setCTime(config.ctime);
    }
    if (config.hasOwnProperty('mtime')) {
      link.setMTime(config.mtime);
    }
    if (config.hasOwnProperty('birthtime')) {
      link.setBirthtime(config.birthtime);
    }
    return link;
  };
}
```
- example usage
```shell
...
});
'''

Note that if you want to create a directory with the default properties, you can provide an 'Object' directly instead of calling
 'mock.directory()'.

### Creating symlinks

Using a 'string' or a 'Buffer' is a shortcut for creating files with default properties.  Using an 'Object' is a shortcut for creating
 a directory with default properties.  There is no shortcut for creating symlinks.  To create a symlink, you need to call the ['
mock.symlink()'](#mocksymlinkproperties) function described below.

### <a id='mocksymlinkproperties'>'mock.symlink(properties)'</a>

Create a factory for new symlinks.  Supported properties:

* **path** - 'string' Path to the source (required).
* **mode** - 'number' Symlink mode (permission and sticky bits).  Defaults to '0666'.
...
```



# <a name="apidoc.module.mock-fs.binding"></a>[module mock-fs.binding](#apidoc.module.mock-fs.binding)

#### <a name="apidoc.element.mock-fs.binding.binding"></a>[function <span class="apidocSignatureSpan">mock-fs.</span>binding (system)](#apidoc.element.mock-fs.binding.binding)
- description and source-code
```javascript
function Binding(system) {

<span class="apidocCodeCommentSpan">  /**
   * Mock file system.
   * @type {FileSystem}
   */
</span>  this._system = system;

  /**
   * Stats constructor.
   * @type {function}
   */
  this.Stats = Stats;

  /**
   * Lookup of open files.
   * @type {Object.<number, FileDescriptor>}
   */
  this._openFiles = {};

  /**
   * Counter for file descriptors.
   * @type {number}
   */
  this._counter = 0;

}
```
- example usage
```shell
...
'''js
// after a test runs
mock.restore();
'''

## Upgrading to version 4

Instead of overriding all methods of the built-in 'fs' module, the library now overrides 'process.binding('fs')'.  The purpose of
 this change is to avoid conflicts with other libraries that override 'fs' methods (e.g. 'graceful-fs') and to make it possible
to work with multiple Node releases without maintaining copied and slightly modified versions of Node's 'fs' module.

Breaking changes:

* The 'mock.fs()' function has been removed.  This returned an object with 'fs'-like methods without overriding the built-in 'fs
' module.
* The object created by 'fs.Stats' is no longer an instance of 'fs.Stats' (though it has all the same properties and methods).
* Lazy 'require()' do not use the real filesystem.
* Tests are no longer run in Node < 4.
...
```



# <a name="apidoc.module.mock-fs.binding.prototype"></a>[module mock-fs.binding.prototype](#apidoc.module.mock-fs.binding.prototype)

#### <a name="apidoc.element.mock-fs.binding.prototype.StatWatcher"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>StatWatcher ()](#apidoc.element.mock-fs.binding.prototype.StatWatcher)
- description and source-code
```javascript
function notImplemented() {
  throw new Error('Method not implemented');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.binding.prototype._getDescriptorById"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>_getDescriptorById (fd)](#apidoc.element.mock-fs.binding.prototype._getDescriptorById)
- description and source-code
```javascript
_getDescriptorById = function (fd) {
  if (!this._openFiles.hasOwnProperty(fd)) {
    throw new FSError('EBADF');
  }
  return this._openFiles[fd];
}
```
- example usage
```shell
...
 * @param {number} fd File descriptor.
 * @param {function(Error, Stats)|Float64Array} callback Callback (optional). In Node 7.7.0+ this will be a Float64Array
 * that should be filled with stat values.
 * @return {Stats|undefined} Stats or undefined (if sync).
 */
Binding.prototype.fstat = function(fd, callback) {
  return maybeCallback(callback, this, function() {
var descriptor = this._getDescriptorById(fd);
var item = descriptor.getItem();
var stats = item.getStats();

// In Node 7.7.0+, binding.stat accepts a Float64Array as the second argument,
// which should be filled with stat values.
// In prior versions of Node, binding.stat simply returns a Stats instance.
if (callback instanceof Float64Array) {
...
```

#### <a name="apidoc.element.mock-fs.binding.prototype._trackDescriptor"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>_trackDescriptor (descriptor)](#apidoc.element.mock-fs.binding.prototype._trackDescriptor)
- description and source-code
```javascript
_trackDescriptor = function (descriptor) {
  var fd = ++this._counter;
  this._openFiles[fd] = descriptor;
  return fd;
}
```
- example usage
```shell
...
   if (descriptor.isTruncate()) {
     item.setContent('');
   }
   if (descriptor.isTruncate() || descriptor.isAppend()) {
     descriptor.setPosition(item.getContent().length);
   }
   descriptor.setItem(item);
   return this._trackDescriptor(descriptor);
 });
};


/**
* Read from a file descriptor.
* @param {string} fd File descriptor.
...
```

#### <a name="apidoc.element.mock-fs.binding.prototype._untrackDescriptorById"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>_untrackDescriptorById (fd)](#apidoc.element.mock-fs.binding.prototype._untrackDescriptorById)
- description and source-code
```javascript
_untrackDescriptorById = function (fd) {
  if (!this._openFiles.hasOwnProperty(fd)) {
    throw new FSError('EBADF');
  }
  delete this._openFiles[fd];
}
```
- example usage
```shell
...
/**
* Close a file descriptor.
* @param {number} fd File descriptor.
* @param {function(Error)} callback Callback (optional).
*/
Binding.prototype.close = function(fd, callback) {
 maybeCallback(callback, this, function() {
   this._untrackDescriptorById(fd);
 });
};


/**
* Open and possibly create a file.
* @param {string} pathname File path.
...
```

#### <a name="apidoc.element.mock-fs.binding.prototype.access"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>access (filepath, mode, callback)](#apidoc.element.mock-fs.binding.prototype.access)
- description and source-code
```javascript
access = function (filepath, mode, callback) {
  maybeCallback(callback, this, function() {
    var item = this._system.getItem(filepath);
    if (!item) {
      throw new FSError('ENOENT', filepath);
    }
    if (mode && process.getuid && process.getgid) {
      var itemMode = item.getMode();
      if (item.getUid() === process.getuid()) {
        if ((itemMode & (mode * 64)) !== mode * 64) {
          throw new FSError('EACCES', filepath);
        }
      } else if (item.getGid() === process.getgid()) {
        if ((itemMode & (mode * 8)) !== mode * 8) {
          throw new FSError('EACCES', filepath);
        }
      } else {
        if ((itemMode & mode) !== mode) {
          throw new FSError('EACCES', filepath);
        }
      }
    }
  });
}
```
- example usage
```shell
...
    if (item) {
      throw new FSError('EEXIST', pathname);
    }
    var parent = this._system.getItem(path.dirname(pathname));
    if (!parent) {
      throw new FSError('ENOENT', pathname);
    }
    this.access(path.dirname(pathname), parseInt('0002', 8));
    var dir = new Directory();
    if (mode) {
      dir.setMode(mode);
    }
    parent.addItem(path.basename(pathname), dir);
  });
};
...
```

#### <a name="apidoc.element.mock-fs.binding.prototype.chmod"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>chmod (pathname, mode, callback)](#apidoc.element.mock-fs.binding.prototype.chmod)
- description and source-code
```javascript
chmod = function (pathname, mode, callback) {
  maybeCallback(callback, this, function() {
    var item = this._system.getItem(pathname);
    if (!item) {
      throw new FSError('ENOENT', pathname);
    }
    item.setMode(mode);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.binding.prototype.chown"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>chown (pathname, uid, gid, callback)](#apidoc.element.mock-fs.binding.prototype.chown)
- description and source-code
```javascript
chown = function (pathname, uid, gid, callback) {
  maybeCallback(callback, this, function() {
    var item = this._system.getItem(pathname);
    if (!item) {
      throw new FSError('ENOENT', pathname);
    }
    item.setUid(uid);
    item.setGid(gid);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.binding.prototype.close"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>close (fd, callback)](#apidoc.element.mock-fs.binding.prototype.close)
- description and source-code
```javascript
close = function (fd, callback) {
  maybeCallback(callback, this, function() {
    this._untrackDescriptorById(fd);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.binding.prototype.fchmod"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>fchmod (fd, mode, callback)](#apidoc.element.mock-fs.binding.prototype.fchmod)
- description and source-code
```javascript
fchmod = function (fd, mode, callback) {
  maybeCallback(callback, this, function() {
    var descriptor = this._getDescriptorById(fd);
    var item = descriptor.getItem();
    item.setMode(mode);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.binding.prototype.fchown"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>fchown (fd, uid, gid, callback)](#apidoc.element.mock-fs.binding.prototype.fchown)
- description and source-code
```javascript
fchown = function (fd, uid, gid, callback) {
  maybeCallback(callback, this, function() {
    var descriptor = this._getDescriptorById(fd);
    var item = descriptor.getItem();
    item.setUid(uid);
    item.setGid(gid);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.binding.prototype.fdatasync"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>fdatasync (fd, callback)](#apidoc.element.mock-fs.binding.prototype.fdatasync)
- description and source-code
```javascript
fdatasync = function (fd, callback) {
  maybeCallback(callback, this, function() {
    this._getDescriptorById(fd);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.binding.prototype.fstat"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>fstat (fd, callback)](#apidoc.element.mock-fs.binding.prototype.fstat)
- description and source-code
```javascript
fstat = function (fd, callback) {
  return maybeCallback(callback, this, function() {
    var descriptor = this._getDescriptorById(fd);
    var item = descriptor.getItem();
    var stats = item.getStats();

    // In Node 7.7.0+, binding.stat accepts a Float64Array as the second argument,
    // which should be filled with stat values.
    // In prior versions of Node, binding.stat simply returns a Stats instance.
    if (callback instanceof Float64Array) {
      fillStatsArray(stats, callback);
    } else {
      return new Stats(stats);
    }
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.binding.prototype.fsync"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>fsync (fd, callback)](#apidoc.element.mock-fs.binding.prototype.fsync)
- description and source-code
```javascript
fsync = function (fd, callback) {
  maybeCallback(callback, this, function() {
    this._getDescriptorById(fd);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.binding.prototype.ftruncate"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>ftruncate (fd, len, callback)](#apidoc.element.mock-fs.binding.prototype.ftruncate)
- description and source-code
```javascript
ftruncate = function (fd, len, callback) {
  maybeCallback(callback, this, function() {
    var descriptor = this._getDescriptorById(fd);
    if (!descriptor.isWrite()) {
      throw new FSError('EINVAL');
    }
    var file = descriptor.getItem();
    if (!(file instanceof File)) {
      throw new FSError('EINVAL');
    }
    var content = file.getContent();
    var newContent = new Buffer(len);
    content.copy(newContent);
    file.setContent(newContent);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.binding.prototype.futimes"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>futimes (fd, atime, mtime, callback)](#apidoc.element.mock-fs.binding.prototype.futimes)
- description and source-code
```javascript
futimes = function (fd, atime, mtime, callback) {
  maybeCallback(callback, this, function() {
    var descriptor = this._getDescriptorById(fd);
    var item = descriptor.getItem();
    item.setATime(new Date(atime * 1000));
    item.setMTime(new Date(mtime * 1000));
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.binding.prototype.getSystem"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>getSystem ()](#apidoc.element.mock-fs.binding.prototype.getSystem)
- description and source-code
```javascript
getSystem = function () {
  return this._system;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.binding.prototype.link"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>link (srcPath, destPath, callback)](#apidoc.element.mock-fs.binding.prototype.link)
- description and source-code
```javascript
link = function (srcPath, destPath, callback) {
  maybeCallback(callback, this, function() {
    var item = this._system.getItem(srcPath);
    if (!item) {
      throw new FSError('ENOENT', srcPath);
    }
    if (item instanceof Directory) {
      throw new FSError('EPERM', srcPath);
    }
    if (this._system.getItem(destPath)) {
      throw new FSError('EEXIST', destPath);
    }
    var parent = this._system.getItem(path.dirname(destPath));
    if (!parent) {
      throw new FSError('ENOENT', destPath);
    }
    if (!(parent instanceof Directory)) {
      throw new FSError('ENOTDIR', destPath);
    }
    parent.addItem(path.basename(destPath), item);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.binding.prototype.lstat"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>lstat (filepath, callback)](#apidoc.element.mock-fs.binding.prototype.lstat)
- description and source-code
```javascript
lstat = function (filepath, callback) {
  return maybeCallback(callback, this, function() {
    var item = this._system.getItem(filepath);
    if (!item) {
      throw new FSError('ENOENT', filepath);
    }
    var stats = item.getStats();

    // In Node 7.7.0+, binding.stat accepts a Float64Array as the second argument,
    // which should be filled with stat values.
    // In prior versions of Node, binding.stat simply returns a Stats instance.
    if (callback instanceof Float64Array) {
      fillStatsArray(stats, callback);
    } else {
      return new Stats(item.getStats());
    }
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.binding.prototype.mkdir"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>mkdir (pathname, mode, callback)](#apidoc.element.mock-fs.binding.prototype.mkdir)
- description and source-code
```javascript
mkdir = function (pathname, mode, callback) {
  maybeCallback(callback, this, function() {
    var item = this._system.getItem(pathname);
    if (item) {
      throw new FSError('EEXIST', pathname);
    }
    var parent = this._system.getItem(path.dirname(pathname));
    if (!parent) {
      throw new FSError('ENOENT', pathname);
    }
    this.access(path.dirname(pathname), parseInt('0002', 8));
    var dir = new Directory();
    if (mode) {
      dir.setMode(mode);
    }
    parent.addItem(path.basename(pathname), dir);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.binding.prototype.open"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>open (pathname, flags, mode, callback)](#apidoc.element.mock-fs.binding.prototype.open)
- description and source-code
```javascript
open = function (pathname, flags, mode, callback) {
  return maybeCallback(callback, this, function() {
    var descriptor = new FileDescriptor(flags);
    var item = this._system.getItem(pathname);
    while (item instanceof SymbolicLink) {
      item = this._system.getItem(
          path.resolve(path.dirname(pathname), item.getPath()));
    }
    if (descriptor.isExclusive() && item) {
      throw new FSError('EEXIST', pathname);
    }
    if (descriptor.isCreate() && !item) {
      var parent = this._system.getItem(path.dirname(pathname));
      if (!parent) {
        throw new FSError('ENOENT', pathname);
      }
      if (!(parent instanceof Directory)) {
        throw new FSError('ENOTDIR', pathname);
      }
      item = new File();
      if (mode) {
        item.setMode(mode);
      }
      parent.addItem(path.basename(pathname), item);
    }
    if (descriptor.isRead()) {
      if (!item) {
        throw new FSError('ENOENT', pathname);
      }
      if (!item.canRead()) {
        throw new FSError('EACCES', pathname);
      }
    }
    if (descriptor.isWrite() && !item.canWrite()) {
      throw new FSError('EACCES', pathname);
    }
    if (descriptor.isTruncate()) {
      item.setContent('');
    }
    if (descriptor.isTruncate() || descriptor.isAppend()) {
      descriptor.setPosition(item.getContent().length);
    }
    descriptor.setItem(item);
    return this._trackDescriptor(descriptor);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.binding.prototype.read"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>read (fd, buffer, offset, length, position, callback)](#apidoc.element.mock-fs.binding.prototype.read)
- description and source-code
```javascript
read = function (fd, buffer, offset, length, position, callback) {
  return maybeCallback(callback, this, function() {
    var descriptor = this._getDescriptorById(fd);
    if (!descriptor.isRead()) {
      throw new FSError('EBADF');
    }
    var file = descriptor.getItem();
    if (!(file instanceof File)) {
      // deleted or not a regular file
      throw new FSError('EBADF');
    }
    if (typeof position !== 'number' || position < 0) {
      position = descriptor.getPosition();
    }
    var content = file.getContent();
    var start = Math.min(position, content.length);
    var end = Math.min(position + length, content.length);
    var read = (start < end) ? content.copy(buffer, offset, start, end) : 0;
    descriptor.setPosition(position + read);
    return read;
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.binding.prototype.readdir"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>readdir (dirpath, encoding, callback)](#apidoc.element.mock-fs.binding.prototype.readdir)
- description and source-code
```javascript
readdir = function (dirpath, encoding, callback) {
  if (encoding && typeof encoding !== 'string') {
    callback = encoding;
    encoding = 'utf-8';
  }
  return maybeCallback(callback, this, function() {
    var dpath = dirpath;
    var dir = this._system.getItem(dirpath);
    while (dir instanceof SymbolicLink) {
      dpath = path.resolve(path.dirname(dpath), dir.getPath());
      dir = this._system.getItem(dpath);
    }
    if (!dir) {
      throw new FSError('ENOENT', dirpath);
    }
    if (!(dir instanceof Directory)) {
      throw new FSError('ENOTDIR', dirpath);
    }
    var list = dir.list();
    if (encoding === 'buffer') {
      list = list.map(function(item) {
        return new Buffer(item);
      });
    }
    return list;
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.binding.prototype.readlink"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>readlink (pathname, encoding, callback)](#apidoc.element.mock-fs.binding.prototype.readlink)
- description and source-code
```javascript
readlink = function (pathname, encoding, callback) {
  if (encoding && typeof encoding !== 'string') {
    callback = encoding;
    encoding = 'utf-8';
  }
  return maybeCallback(callback, this, function() {
    var link = this._system.getItem(pathname);
    if (!(link instanceof SymbolicLink)) {
      throw new FSError('EINVAL', pathname);
    }
    var linkPath = link.getPath();
    if (encoding === 'buffer') {
      linkPath = new Buffer(linkPath);
    }
    return linkPath;
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.binding.prototype.realpath"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>realpath (filepath, encoding, callback)](#apidoc.element.mock-fs.binding.prototype.realpath)
- description and source-code
```javascript
realpath = function (filepath, encoding, callback) {
  return maybeCallback(callback, this, function() {
    var realPath;
    if (Buffer.isBuffer(filepath)) {
      filepath = filepath.toString();
    }
    var resolved = path.resolve(filepath);
    var parts = getPathParts(resolved);
    var item = this._system.getRoot();
    var itemPath = '/';
    var name, i, ii;
    for (i = 0, ii = parts.length; i < ii; ++i) {
      name = parts[i];
      while (item instanceof SymbolicLink) {
        itemPath = path.resolve(path.dirname(itemPath), item.getPath());
        item = this._system.getItem(itemPath);
      }
      if (!item) {
        throw new FSError('ENOENT', filepath);
      }
      if (item instanceof Directory) {
        itemPath = path.resolve(itemPath, name);
        item = item.getItem(name);
      } else {
        throw new FSError('ENOTDIR', filepath);
      }
    }
    if (item) {
      while (item instanceof SymbolicLink) {
        itemPath = path.resolve(path.dirname(itemPath), item.getPath());
        item = this._system.getItem(itemPath);
      }
      realPath = itemPath;
    } else {
      throw new FSError('ENOENT', filepath);
    }

    if (encoding === 'buffer') {
      realPath = new Buffer(realPath);
    }
    return realPath;
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.binding.prototype.rename"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>rename (oldPath, newPath, callback)](#apidoc.element.mock-fs.binding.prototype.rename)
- description and source-code
```javascript
rename = function (oldPath, newPath, callback) {
  return maybeCallback(callback, this, function() {
    var oldItem = this._system.getItem(oldPath);
    if (!oldItem) {
      throw new FSError('ENOENT', oldPath);
    }
    var oldParent = this._system.getItem(path.dirname(oldPath));
    var oldName = path.basename(oldPath);
    var newItem = this._system.getItem(newPath);
    var newParent = this._system.getItem(path.dirname(newPath));
    var newName = path.basename(newPath);
    if (newItem) {
      // make sure they are the same type
      if (oldItem instanceof File) {
        if (newItem instanceof Directory) {
          throw new FSError('EISDIR', newPath);
        }
      } else if (oldItem instanceof Directory) {
        if (!(newItem instanceof Directory)) {
          throw new FSError('ENOTDIR', newPath);
        }
        if (newItem.list().length > 0) {
          throw new FSError('ENOTEMPTY', newPath);
        }
      }
      newParent.removeItem(newName);
    } else {
      if (!newParent) {
        throw new FSError('ENOENT', newPath);
      }
      if (!(newParent instanceof Directory)) {
        throw new FSError('ENOTDIR', newPath);
      }
    }
    oldParent.removeItem(oldName);
    newParent.addItem(newName, oldItem);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.binding.prototype.rmdir"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>rmdir (pathname, callback)](#apidoc.element.mock-fs.binding.prototype.rmdir)
- description and source-code
```javascript
rmdir = function (pathname, callback) {
  maybeCallback(callback, this, function() {
    var item = this._system.getItem(pathname);
    if (!item) {
      throw new FSError('ENOENT', pathname);
    }
    if (!(item instanceof Directory)) {
      throw new FSError('ENOTDIR', pathname);
    }
    if (item.list().length > 0) {
      throw new FSError('ENOTEMPTY', pathname);
    }
    this.access(path.dirname(pathname), parseInt('0002', 8));
    var parent = this._system.getItem(path.dirname(pathname));
    parent.removeItem(path.basename(pathname));
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.binding.prototype.setSystem"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>setSystem (system)](#apidoc.element.mock-fs.binding.prototype.setSystem)
- description and source-code
```javascript
setSystem = function (system) {
  this._system = system;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.binding.prototype.stat"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>stat (filepath, callback)](#apidoc.element.mock-fs.binding.prototype.stat)
- description and source-code
```javascript
stat = function (filepath, callback) {
  return maybeCallback(callback, this, function() {
    var item = this._system.getItem(filepath);
    if (item instanceof SymbolicLink) {
      item = this._system.getItem(
          path.resolve(path.dirname(filepath), item.getPath()));
    }
    if (!item) {
      throw new FSError('ENOENT', filepath);
    }
    var stats = item.getStats();

    // In Node 7.7.0+, binding.stat accepts a Float64Array as the second argument,
    // which should be filled with stat values.
    // In prior versions of Node, binding.stat simply returns a Stats instance.
    if (callback instanceof Float64Array) {
      fillStatsArray(stats, callback);
    } else {
      return new Stats(stats);
    }
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.binding.prototype.symlink"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>symlink (srcPath, destPath, type, callback)](#apidoc.element.mock-fs.binding.prototype.symlink)
- description and source-code
```javascript
symlink = function (srcPath, destPath, type, callback) {
  maybeCallback(callback, this, function() {
    if (this._system.getItem(destPath)) {
      throw new FSError('EEXIST', destPath);
    }
    var parent = this._system.getItem(path.dirname(destPath));
    if (!parent) {
      throw new FSError('ENOENT', destPath);
    }
    if (!(parent instanceof Directory)) {
      throw new FSError('ENOTDIR', destPath);
    }
    var link = new SymbolicLink();
    link.setPath(srcPath);
    parent.addItem(path.basename(destPath), link);
  });
}
```
- example usage
```shell
...
});
'''

Note that if you want to create a directory with the default properties, you can provide an 'Object' directly instead of calling
 'mock.directory()'.

### Creating symlinks

Using a 'string' or a 'Buffer' is a shortcut for creating files with default properties.  Using an 'Object' is a shortcut for creating
 a directory with default properties.  There is no shortcut for creating symlinks.  To create a symlink, you need to call the ['
mock.symlink()'](#mocksymlinkproperties) function described below.

### <a id='mocksymlinkproperties'>'mock.symlink(properties)'</a>

Create a factory for new symlinks.  Supported properties:

* **path** - 'string' Path to the source (required).
* **mode** - 'number' Symlink mode (permission and sticky bits).  Defaults to '0666'.
...
```

#### <a name="apidoc.element.mock-fs.binding.prototype.truncate"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>truncate (fd, len, callback)](#apidoc.element.mock-fs.binding.prototype.truncate)
- description and source-code
```javascript
truncate = function (fd, len, callback) {
  maybeCallback(callback, this, function() {
    var descriptor = this._getDescriptorById(fd);
    if (!descriptor.isWrite()) {
      throw new FSError('EINVAL');
    }
    var file = descriptor.getItem();
    if (!(file instanceof File)) {
      throw new FSError('EINVAL');
    }
    var content = file.getContent();
    var newContent = new Buffer(len);
    content.copy(newContent);
    file.setContent(newContent);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.binding.prototype.unlink"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>unlink (pathname, callback)](#apidoc.element.mock-fs.binding.prototype.unlink)
- description and source-code
```javascript
unlink = function (pathname, callback) {
  maybeCallback(callback, this, function() {
    var item = this._system.getItem(pathname);
    if (!item) {
      throw new FSError('ENOENT', pathname);
    }
    if (item instanceof Directory) {
      throw new FSError('EPERM', pathname);
    }
    var parent = this._system.getItem(path.dirname(pathname));
    parent.removeItem(path.basename(pathname));
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.binding.prototype.utimes"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>utimes (pathname, atime, mtime, callback)](#apidoc.element.mock-fs.binding.prototype.utimes)
- description and source-code
```javascript
utimes = function (pathname, atime, mtime, callback) {
  maybeCallback(callback, this, function() {
    var item = this._system.getItem(pathname);
    if (!item) {
      throw new FSError('ENOENT', pathname);
    }
    item.setATime(new Date(atime * 1000));
    item.setMTime(new Date(mtime * 1000));
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.binding.prototype.write"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>write (fd, buffer, offset, length, position, callback)](#apidoc.element.mock-fs.binding.prototype.write)
- description and source-code
```javascript
write = function (fd, buffer, offset, length, position, callback) {
  return maybeCallback(callback, this, function() {
    var descriptor = this._getDescriptorById(fd);
    if (!descriptor.isWrite()) {
      throw new FSError('EBADF');
    }
    var file = descriptor.getItem();
    if (!(file instanceof File)) {
      // not a regular file
      throw new FSError('EBADF');
    }
    if (typeof position !== 'number' || position < 0) {
      position = descriptor.getPosition();
    }
    var content = file.getContent();
    var newLength = position + length;
    if (content.length < newLength) {
      var newContent = new Buffer(newLength);
      content.copy(newContent);
      content = newContent;
    }
    var sourceEnd = Math.min(offset + length, buffer.length);
    var written = buffer.copy(content, position, offset, sourceEnd);
    file.setContent(content);
    descriptor.setPosition(newLength);
    return written;
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.binding.prototype.writeBuffer"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>writeBuffer (fd, buffer, offset, length, position, callback)](#apidoc.element.mock-fs.binding.prototype.writeBuffer)
- description and source-code
```javascript
writeBuffer = function (fd, buffer, offset, length, position, callback) {
  return maybeCallback(callback, this, function() {
    var descriptor = this._getDescriptorById(fd);
    if (!descriptor.isWrite()) {
      throw new FSError('EBADF');
    }
    var file = descriptor.getItem();
    if (!(file instanceof File)) {
      // not a regular file
      throw new FSError('EBADF');
    }
    if (typeof position !== 'number' || position < 0) {
      position = descriptor.getPosition();
    }
    var content = file.getContent();
    var newLength = position + length;
    if (content.length < newLength) {
      var newContent = new Buffer(newLength);
      content.copy(newContent);
      content = newContent;
    }
    var sourceEnd = Math.min(offset + length, buffer.length);
    var written = buffer.copy(content, position, offset, sourceEnd);
    file.setContent(content);
    descriptor.setPosition(newLength);
    return written;
  });
}
```
- example usage
```shell
...
   if (callback.oncomplete) {
     callback = callback.oncomplete.bind(callback);
   }
   wrapper = function(err, written, returned) {
     callback(err, written, returned && string);
   };
 }
 return this.writeBuffer(fd, buffer, 0, string.length, position, wrapper);
};


/**
* Rename a file.
* @param {string} oldPath Old pathname.
* @param {string} newPath New pathname.
...
```

#### <a name="apidoc.element.mock-fs.binding.prototype.writeBuffers"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>writeBuffers (fd, buffers, position, callback)](#apidoc.element.mock-fs.binding.prototype.writeBuffers)
- description and source-code
```javascript
writeBuffers = function (fd, buffers, position, callback) {
  return maybeCallback(callback, this, function() {
    var descriptor = this._getDescriptorById(fd);
    if (!descriptor.isWrite()) {
      throw new FSError('EBADF');
    }
    var file = descriptor.getItem();
    if (!(file instanceof File)) {
      // not a regular file
      throw new FSError('EBADF');
    }
    if (typeof position !== 'number' || position < 0) {
      position = descriptor.getPosition();
    }
    var content = file.getContent();
    var newContent = Buffer.concat(buffers);
    var newLength = position + newContent.length;
    if (content.length < newLength) {
      var tempContent = new Buffer(newLength);
      content.copy(tempContent);
      content = tempContent;
    }
    var written = newContent.copy(content, position);
    file.setContent(content);
    descriptor.setPosition(newLength);
    return written;
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.binding.prototype.writeString"></a>[function <span class="apidocSignatureSpan">mock-fs.binding.prototype.</span>writeString (fd, string, position, encoding, callback)](#apidoc.element.mock-fs.binding.prototype.writeString)
- description and source-code
```javascript
writeString = function (fd, string, position, encoding, callback) {
  var buffer = new Buffer(string, encoding);
  var wrapper;
  if (callback) {
    if (callback.oncomplete) {
      callback = callback.oncomplete.bind(callback);
    }
    wrapper = function(err, written, returned) {
      callback(err, written, returned && string);
    };
  }
  return this.writeBuffer(fd, buffer, 0, string.length, position, wrapper);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mock-fs.descriptor"></a>[module mock-fs.descriptor](#apidoc.module.mock-fs.descriptor)

#### <a name="apidoc.element.mock-fs.descriptor.descriptor"></a>[function <span class="apidocSignatureSpan">mock-fs.</span>descriptor (flags)](#apidoc.element.mock-fs.descriptor.descriptor)
- description and source-code
```javascript
function FileDescriptor(flags) {

<span class="apidocCodeCommentSpan">  /**
   * Flags.
   * @type {number}
   */
</span>  this._flags = flags;

  /**
   * File system item.
   * @type {Item}
   */
  this._item = null;

  /**
   * Current file position.
   * @type {number}
   */
  this._position = 0;

}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mock-fs.descriptor.prototype"></a>[module mock-fs.descriptor.prototype](#apidoc.module.mock-fs.descriptor.prototype)

#### <a name="apidoc.element.mock-fs.descriptor.prototype.getItem"></a>[function <span class="apidocSignatureSpan">mock-fs.descriptor.prototype.</span>getItem ()](#apidoc.element.mock-fs.descriptor.prototype.getItem)
- description and source-code
```javascript
getItem = function () {
  return this._item;
}
```
- example usage
```shell
...
var item = this._system.getRoot();
var itemPath = '/';
var name, i, ii;
for (i = 0, ii = parts.length; i < ii; ++i) {
  name = parts[i];
  while (item instanceof SymbolicLink) {
    itemPath = path.resolve(path.dirname(itemPath), item.getPath());
    item = this._system.getItem(itemPath);
  }
  if (!item) {
    throw new FSError('ENOENT', filepath);
  }
  if (item instanceof Directory) {
    itemPath = path.resolve(itemPath, name);
    item = item.getItem(name);
...
```

#### <a name="apidoc.element.mock-fs.descriptor.prototype.getPosition"></a>[function <span class="apidocSignatureSpan">mock-fs.descriptor.prototype.</span>getPosition ()](#apidoc.element.mock-fs.descriptor.prototype.getPosition)
- description and source-code
```javascript
getPosition = function () {
  return this._position;
}
```
- example usage
```shell
...
}
var file = descriptor.getItem();
if (!(file instanceof File)) {
  // deleted or not a regular file
  throw new FSError('EBADF');
}
if (typeof position !== 'number' || position < 0) {
  position = descriptor.getPosition();
}
var content = file.getContent();
var start = Math.min(position, content.length);
var end = Math.min(position + length, content.length);
var read = (start < end) ? content.copy(buffer, offset, start, end) : 0;
descriptor.setPosition(position + read);
return read;
...
```

#### <a name="apidoc.element.mock-fs.descriptor.prototype.isAppend"></a>[function <span class="apidocSignatureSpan">mock-fs.descriptor.prototype.</span>isAppend ()](#apidoc.element.mock-fs.descriptor.prototype.isAppend)
- description and source-code
```javascript
isAppend = function () {
  return ((this._flags & constants.O_APPEND) === constants.O_APPEND);
}
```
- example usage
```shell
...
    }
    if (descriptor.isWrite() && !item.canWrite()) {
      throw new FSError('EACCES', pathname);
    }
    if (descriptor.isTruncate()) {
      item.setContent('');
    }
    if (descriptor.isTruncate() || descriptor.isAppend()) {
      descriptor.setPosition(item.getContent().length);
    }
    descriptor.setItem(item);
    return this._trackDescriptor(descriptor);
  });
};
...
```

#### <a name="apidoc.element.mock-fs.descriptor.prototype.isCreate"></a>[function <span class="apidocSignatureSpan">mock-fs.descriptor.prototype.</span>isCreate ()](#apidoc.element.mock-fs.descriptor.prototype.isCreate)
- description and source-code
```javascript
isCreate = function () {
  return ((this._flags & constants.O_CREAT) === constants.O_CREAT);
}
```
- example usage
```shell
...
while (item instanceof SymbolicLink) {
  item = this._system.getItem(
      path.resolve(path.dirname(pathname), item.getPath()));
}
if (descriptor.isExclusive() && item) {
  throw new FSError('EEXIST', pathname);
}
if (descriptor.isCreate() && !item) {
  var parent = this._system.getItem(path.dirname(pathname));
  if (!parent) {
    throw new FSError('ENOENT', pathname);
  }
  if (!(parent instanceof Directory)) {
    throw new FSError('ENOTDIR', pathname);
  }
...
```

#### <a name="apidoc.element.mock-fs.descriptor.prototype.isExclusive"></a>[function <span class="apidocSignatureSpan">mock-fs.descriptor.prototype.</span>isExclusive ()](#apidoc.element.mock-fs.descriptor.prototype.isExclusive)
- description and source-code
```javascript
isExclusive = function () {
  return ((this._flags & constants.O_EXCL) === constants.O_EXCL);
}
```
- example usage
```shell
...
  return maybeCallback(callback, this, function() {
var descriptor = new FileDescriptor(flags);
var item = this._system.getItem(pathname);
while (item instanceof SymbolicLink) {
  item = this._system.getItem(
      path.resolve(path.dirname(pathname), item.getPath()));
}
if (descriptor.isExclusive() && item) {
  throw new FSError('EEXIST', pathname);
}
if (descriptor.isCreate() && !item) {
  var parent = this._system.getItem(path.dirname(pathname));
  if (!parent) {
    throw new FSError('ENOENT', pathname);
  }
...
```

#### <a name="apidoc.element.mock-fs.descriptor.prototype.isRead"></a>[function <span class="apidocSignatureSpan">mock-fs.descriptor.prototype.</span>isRead ()](#apidoc.element.mock-fs.descriptor.prototype.isRead)
- description and source-code
```javascript
isRead = function () {
  // special treatment because O_RDONLY is 0
  return (this._flags === constants.O_RDONLY) ||
      (this._flags === (constants.O_RDONLY | constants.O_SYNC)) ||
      ((this._flags & constants.O_RDWR) === constants.O_RDWR);
}
```
- example usage
```shell
...
  }
  item = new File();
  if (mode) {
    item.setMode(mode);
  }
  parent.addItem(path.basename(pathname), item);
}
if (descriptor.isRead()) {
  if (!item) {
    throw new FSError('ENOENT', pathname);
  }
  if (!item.canRead()) {
    throw new FSError('EACCES', pathname);
  }
}
...
```

#### <a name="apidoc.element.mock-fs.descriptor.prototype.isTruncate"></a>[function <span class="apidocSignatureSpan">mock-fs.descriptor.prototype.</span>isTruncate ()](#apidoc.element.mock-fs.descriptor.prototype.isTruncate)
- description and source-code
```javascript
isTruncate = function () {
  return (this._flags & constants.O_TRUNC) === constants.O_TRUNC;
}
```
- example usage
```shell
...
  if (!item.canRead()) {
    throw new FSError('EACCES', pathname);
  }
}
if (descriptor.isWrite() && !item.canWrite()) {
  throw new FSError('EACCES', pathname);
}
if (descriptor.isTruncate()) {
  item.setContent('');
}
if (descriptor.isTruncate() || descriptor.isAppend()) {
  descriptor.setPosition(item.getContent().length);
}
descriptor.setItem(item);
return this._trackDescriptor(descriptor);
...
```

#### <a name="apidoc.element.mock-fs.descriptor.prototype.isWrite"></a>[function <span class="apidocSignatureSpan">mock-fs.descriptor.prototype.</span>isWrite ()](#apidoc.element.mock-fs.descriptor.prototype.isWrite)
- description and source-code
```javascript
isWrite = function () {
  return ((this._flags & constants.O_WRONLY) === constants.O_WRONLY) ||
      ((this._flags & constants.O_RDWR) === constants.O_RDWR);
}
```
- example usage
```shell
...
  if (!item) {
    throw new FSError('ENOENT', pathname);
  }
  if (!item.canRead()) {
    throw new FSError('EACCES', pathname);
  }
}
if (descriptor.isWrite() && !item.canWrite()) {
  throw new FSError('EACCES', pathname);
}
if (descriptor.isTruncate()) {
  item.setContent('');
}
if (descriptor.isTruncate() || descriptor.isAppend()) {
  descriptor.setPosition(item.getContent().length);
...
```

#### <a name="apidoc.element.mock-fs.descriptor.prototype.setItem"></a>[function <span class="apidocSignatureSpan">mock-fs.descriptor.prototype.</span>setItem (item)](#apidoc.element.mock-fs.descriptor.prototype.setItem)
- description and source-code
```javascript
setItem = function (item) {
  this._item = item;
}
```
- example usage
```shell
...
   }
   if (descriptor.isTruncate()) {
     item.setContent('');
   }
   if (descriptor.isTruncate() || descriptor.isAppend()) {
     descriptor.setPosition(item.getContent().length);
   }
   descriptor.setItem(item);
   return this._trackDescriptor(descriptor);
 });
};


/**
* Read from a file descriptor.
...
```

#### <a name="apidoc.element.mock-fs.descriptor.prototype.setPosition"></a>[function <span class="apidocSignatureSpan">mock-fs.descriptor.prototype.</span>setPosition (position)](#apidoc.element.mock-fs.descriptor.prototype.setPosition)
- description and source-code
```javascript
setPosition = function (position) {
  this._position = position;
}
```
- example usage
```shell
...
    if (descriptor.isWrite() && !item.canWrite()) {
      throw new FSError('EACCES', pathname);
    }
    if (descriptor.isTruncate()) {
      item.setContent('');
    }
    if (descriptor.isTruncate() || descriptor.isAppend()) {
      descriptor.setPosition(item.getContent().length);
    }
    descriptor.setItem(item);
    return this._trackDescriptor(descriptor);
  });
};
...
```



# <a name="apidoc.module.mock-fs.directory"></a>[module mock-fs.directory](#apidoc.module.mock-fs.directory)

#### <a name="apidoc.element.mock-fs.directory.directory"></a>[function <span class="apidocSignatureSpan">mock-fs.</span>directory ()](#apidoc.element.mock-fs.directory.directory)
- description and source-code
```javascript
function Directory() {
  Item.call(this);

<span class="apidocCodeCommentSpan">  /**
   * Items in this directory.
   * @type {Object.<string, Item>}
   */
</span>  this._items = {};

  /**
   * Permissions.
   */
  this._mode = 511; // 0777

}
```
- example usage
```shell
...
       file2: new Buffer([1, 2, 3, 4])
     }
   }
 }
});
'''

To create a directory with additional properties (owner, permissions, atime, etc.), use the ['mock.directory()'](mockdirectoryproperties
) function described below.

### <a id='mockdirectoryproperties'>'mock.directory(properties)'</a>

Create a factory for new directories.  Supported properties:

* **mode** - 'number' Directory mode (permission and sticky bits).  Defaults to '0777'.
* **uid** - 'number' The user id.  Defaults to 'process.getuid()'.
...
```

#### <a name="apidoc.element.mock-fs.directory.super_"></a>[function <span class="apidocSignatureSpan">mock-fs.directory.</span>super_ ()](#apidoc.element.mock-fs.directory.super_)
- description and source-code
```javascript
function Item() {

  var now = Date.now();

<span class="apidocCodeCommentSpan">  /**
   * Access time.
   * @type {Date}
   */
</span>  this._atime = new Date(now);

  /**
   * Change time.
   * @type {Date}
   */
  this._ctime = new Date(now);

  /**
   * Birth time.
   * @type {Date}
   */
  this._birthtime = new Date(now);

  /**
   * Modification time.
   * @type {Date}
   */
  this._mtime = new Date(now);

  /**
   * Permissions.
   */
  this._mode = 438; // 0666

  /**
   * User id.
   * @type {number}
   */
  this._uid = getUid();

  /**
   * Group id.
   * @type {number}
   */
  this._gid = getGid();

  /**
   * Item number.
   * @type {number}
   */
  this._id = ++counter;

  /**
   * Number of links to this item.
   */
  this.links = 0;

}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mock-fs.directory.prototype"></a>[module mock-fs.directory.prototype](#apidoc.module.mock-fs.directory.prototype)

#### <a name="apidoc.element.mock-fs.directory.prototype.addItem"></a>[function <span class="apidocSignatureSpan">mock-fs.directory.prototype.</span>addItem (name, item)](#apidoc.element.mock-fs.directory.prototype.addItem)
- description and source-code
```javascript
addItem = function (name, item) {
  if (this._items.hasOwnProperty(name)) {
    throw new Error('Item with the same name already exists: ' + name);
  }
  this._items[name] = item;
  ++item.links;
  if (item instanceof Directory) {
    // for '.' entry
    ++item.links;
    // for subdirectory
    ++this.links;
  }
  this.setMTime(new Date());
  return item;
}
```
- example usage
```shell
...
  if (!(parent instanceof Directory)) {
    throw new FSError('ENOTDIR', pathname);
  }
  item = new File();
  if (mode) {
    item.setMode(mode);
  }
  parent.addItem(path.basename(pathname), item);
}
if (descriptor.isRead()) {
  if (!item) {
    throw new FSError('ENOENT', pathname);
  }
  if (!item.canRead()) {
    throw new FSError('EACCES', pathname);
...
```

#### <a name="apidoc.element.mock-fs.directory.prototype.getItem"></a>[function <span class="apidocSignatureSpan">mock-fs.directory.prototype.</span>getItem (name)](#apidoc.element.mock-fs.directory.prototype.getItem)
- description and source-code
```javascript
getItem = function (name) {
  var item = null;
  if (this._items.hasOwnProperty(name)) {
    item = this._items[name];
  }
  return item;
}
```
- example usage
```shell
...
var item = this._system.getRoot();
var itemPath = '/';
var name, i, ii;
for (i = 0, ii = parts.length; i < ii; ++i) {
  name = parts[i];
  while (item instanceof SymbolicLink) {
    itemPath = path.resolve(path.dirname(itemPath), item.getPath());
    item = this._system.getItem(itemPath);
  }
  if (!item) {
    throw new FSError('ENOENT', filepath);
  }
  if (item instanceof Directory) {
    itemPath = path.resolve(itemPath, name);
    item = item.getItem(name);
...
```

#### <a name="apidoc.element.mock-fs.directory.prototype.getStats"></a>[function <span class="apidocSignatureSpan">mock-fs.directory.prototype.</span>getStats ()](#apidoc.element.mock-fs.directory.prototype.getStats)
- description and source-code
```javascript
getStats = function () {
  var stats = Item.prototype.getStats.call(this);
  stats.mode = this.getMode() | constants.S_IFDIR;
  stats.size = 1;
  stats.blocks = 1;
  return stats;
}
```
- example usage
```shell
...
if (item instanceof SymbolicLink) {
  item = this._system.getItem(
      path.resolve(path.dirname(filepath), item.getPath()));
}
if (!item) {
  throw new FSError('ENOENT', filepath);
}
var stats = item.getStats();

// In Node 7.7.0+, binding.stat accepts a Float64Array as the second argument,
// which should be filled with stat values.
// In prior versions of Node, binding.stat simply returns a Stats instance.
if (callback instanceof Float64Array) {
  fillStatsArray(stats, callback);
} else {
...
```

#### <a name="apidoc.element.mock-fs.directory.prototype.list"></a>[function <span class="apidocSignatureSpan">mock-fs.directory.prototype.</span>list ()](#apidoc.element.mock-fs.directory.prototype.list)
- description and source-code
```javascript
list = function () {
  return Object.keys(this._items).sort();
}
```
- example usage
```shell
...
    if (newItem instanceof Directory) {
      throw new FSError('EISDIR', newPath);
    }
  } else if (oldItem instanceof Directory) {
    if (!(newItem instanceof Directory)) {
      throw new FSError('ENOTDIR', newPath);
    }
    if (newItem.list().length > 0) {
      throw new FSError('ENOTEMPTY', newPath);
    }
  }
  newParent.removeItem(newName);
} else {
  if (!newParent) {
    throw new FSError('ENOENT', newPath);
...
```

#### <a name="apidoc.element.mock-fs.directory.prototype.removeItem"></a>[function <span class="apidocSignatureSpan">mock-fs.directory.prototype.</span>removeItem (name)](#apidoc.element.mock-fs.directory.prototype.removeItem)
- description and source-code
```javascript
removeItem = function (name) {
  if (!this._items.hasOwnProperty(name)) {
    throw new Error('Item does not exist in directory: ' + name);
  }
  var item = this._items[name];
  delete this._items[name];
  --item.links;
  if (item instanceof Directory) {
    // for '.' entry
    --item.links;
    // for subdirectory
    --this.links;
  }
  this.setMTime(new Date());
  return item;
}
```
- example usage
```shell
...
    if (!(newItem instanceof Directory)) {
      throw new FSError('ENOTDIR', newPath);
    }
    if (newItem.list().length > 0) {
      throw new FSError('ENOTEMPTY', newPath);
    }
  }
  newParent.removeItem(newName);
} else {
  if (!newParent) {
    throw new FSError('ENOENT', newPath);
  }
  if (!(newParent instanceof Directory)) {
    throw new FSError('ENOTDIR', newPath);
  }
...
```



# <a name="apidoc.module.mock-fs.file"></a>[module mock-fs.file](#apidoc.module.mock-fs.file)

#### <a name="apidoc.element.mock-fs.file.file"></a>[function <span class="apidocSignatureSpan">mock-fs.</span>file ()](#apidoc.element.mock-fs.file.file)
- description and source-code
```javascript
function File() {
  Item.call(this);

<span class="apidocCodeCommentSpan">  /**
   * File content.
   * @type {Buffer}
   */
</span>  this._content = EMPTY;

}
```
- example usage
```shell
...
When 'config' property values are a 'string' or 'Buffer', a file is created with the provided content.  For example, the following
 configuration creates a single file with string content (in addition to the two default directories).
'''js
mock({
 'path/to/file.txt': 'file content here'
});
'''

To create a file with additional properties (owner, permissions, atime, etc.), use the ['mock.file()'](#mockfileproperties) function
 described below.

### <a id='mockfileproperties'>'mock.file(properties)'</a>

Create a factory for new files.  Supported properties:

* **content** - 'string|Buffer' File contents.
* **mode** - 'number' File mode (permission and sticky bits).  Defaults to '0666'.
...
```

#### <a name="apidoc.element.mock-fs.file.super_"></a>[function <span class="apidocSignatureSpan">mock-fs.file.</span>super_ ()](#apidoc.element.mock-fs.file.super_)
- description and source-code
```javascript
function Item() {

  var now = Date.now();

<span class="apidocCodeCommentSpan">  /**
   * Access time.
   * @type {Date}
   */
</span>  this._atime = new Date(now);

  /**
   * Change time.
   * @type {Date}
   */
  this._ctime = new Date(now);

  /**
   * Birth time.
   * @type {Date}
   */
  this._birthtime = new Date(now);

  /**
   * Modification time.
   * @type {Date}
   */
  this._mtime = new Date(now);

  /**
   * Permissions.
   */
  this._mode = 438; // 0666

  /**
   * User id.
   * @type {number}
   */
  this._uid = getUid();

  /**
   * Group id.
   * @type {number}
   */
  this._gid = getGid();

  /**
   * Item number.
   * @type {number}
   */
  this._id = ++counter;

  /**
   * Number of links to this item.
   */
  this.links = 0;

}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mock-fs.file.prototype"></a>[module mock-fs.file.prototype](#apidoc.module.mock-fs.file.prototype)

#### <a name="apidoc.element.mock-fs.file.prototype.getContent"></a>[function <span class="apidocSignatureSpan">mock-fs.file.prototype.</span>getContent ()](#apidoc.element.mock-fs.file.prototype.getContent)
- description and source-code
```javascript
getContent = function () {
  this.setATime(new Date());
  return this._content;
}
```
- example usage
```shell
...
    if (descriptor.isWrite() && !item.canWrite()) {
      throw new FSError('EACCES', pathname);
    }
    if (descriptor.isTruncate()) {
      item.setContent('');
    }
    if (descriptor.isTruncate() || descriptor.isAppend()) {
      descriptor.setPosition(item.getContent().length);
    }
    descriptor.setItem(item);
    return this._trackDescriptor(descriptor);
  });
};
...
```

#### <a name="apidoc.element.mock-fs.file.prototype.getStats"></a>[function <span class="apidocSignatureSpan">mock-fs.file.prototype.</span>getStats ()](#apidoc.element.mock-fs.file.prototype.getStats)
- description and source-code
```javascript
getStats = function () {
  var size = this._content.length;
  var stats = Item.prototype.getStats.call(this);
  stats.mode = this.getMode() | constants.S_IFREG;
  stats.size = size;
  stats.blocks = Math.ceil(size / 512);
  return stats;
}
```
- example usage
```shell
...
if (item instanceof SymbolicLink) {
  item = this._system.getItem(
      path.resolve(path.dirname(filepath), item.getPath()));
}
if (!item) {
  throw new FSError('ENOENT', filepath);
}
var stats = item.getStats();

// In Node 7.7.0+, binding.stat accepts a Float64Array as the second argument,
// which should be filled with stat values.
// In prior versions of Node, binding.stat simply returns a Stats instance.
if (callback instanceof Float64Array) {
  fillStatsArray(stats, callback);
} else {
...
```

#### <a name="apidoc.element.mock-fs.file.prototype.setContent"></a>[function <span class="apidocSignatureSpan">mock-fs.file.prototype.</span>setContent (content)](#apidoc.element.mock-fs.file.prototype.setContent)
- description and source-code
```javascript
setContent = function (content) {
  if (typeof content === 'string') {
    content = new Buffer(content);
  } else if (!Buffer.isBuffer(content)) {
    throw new Error('File content must be a string or buffer');
  }
  this._content = content;
  var now = Date.now();
  this.setCTime(new Date(now));
  this.setMTime(new Date(now));
}
```
- example usage
```shell
...
      throw new FSError('EACCES', pathname);
    }
  }
  if (descriptor.isWrite() && !item.canWrite()) {
    throw new FSError('EACCES', pathname);
  }
  if (descriptor.isTruncate()) {
    item.setContent('');
  }
  if (descriptor.isTruncate() || descriptor.isAppend()) {
    descriptor.setPosition(item.getContent().length);
  }
  descriptor.setItem(item);
  return this._trackDescriptor(descriptor);
});
...
```



# <a name="apidoc.module.mock-fs.filesystem"></a>[module mock-fs.filesystem](#apidoc.module.mock-fs.filesystem)

#### <a name="apidoc.element.mock-fs.filesystem.filesystem"></a>[function <span class="apidocSignatureSpan">mock-fs.</span>filesystem (options)](#apidoc.element.mock-fs.filesystem.filesystem)
- description and source-code
```javascript
function FileSystem(options) {
  options = options || {};

  var createCwd = 'createCwd' in options ? options.createCwd : true;
  var createTmp = 'createTmp' in options ? options.createTmp : true;

  var root = new Directory();

  // populate with default directories
  var defaults = [];
  if (createCwd) {
    defaults.push(process.cwd());
  }

  if (createTmp) {
    defaults.push(os.tmpdir && os.tmpdir() || os.tmpDir());
  }

  defaults.forEach(function(dir) {
    var parts = getPathParts(dir);
    var directory = root;
    var i, ii, name, candidate;
    for (i = 0, ii = parts.length; i < ii; ++i) {
      name = parts[i];
      candidate = directory.getItem(name);
      if (!candidate) {
        directory = directory.addItem(name, new Directory());
      } else if (candidate instanceof Directory) {
        directory = candidate;
      } else {
        throw new Error('Failed to create directory: ' + dir);
      }
    }
  });

<span class="apidocCodeCommentSpan">  /**
   * Root directory.
   * @type {Directory}
   */
</span>  this._root = root;

}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.filesystem.create"></a>[function <span class="apidocSignatureSpan">mock-fs.filesystem.</span>create (paths, options)](#apidoc.element.mock-fs.filesystem.create)
- description and source-code
```javascript
create = function (paths, options) {
  var system = new FileSystem(options);

  for (var filepath in paths) {
    var parts = getPathParts(filepath);
    var directory = system._root;
    var i, ii, name, candidate;
    for (i = 0, ii = parts.length - 1; i < ii; ++i) {
      name = parts[i];
      candidate = directory.getItem(name);
      if (!candidate) {
        directory = directory.addItem(name, new Directory());
      } else if (candidate instanceof Directory) {
        directory = candidate;
      } else {
        throw new Error('Failed to create directory: ' + filepath);
      }
    }
    populate(directory, parts[i], paths[filepath]);
  }

  return system;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.filesystem.directory"></a>[function <span class="apidocSignatureSpan">mock-fs.filesystem.</span>directory (config)](#apidoc.element.mock-fs.filesystem.directory)
- description and source-code
```javascript
directory = function (config) {
  config = config || {};
  return function() {
    var dir = new Directory();
    if (config.hasOwnProperty('mode')) {
      dir.setMode(config.mode);
    }
    if (config.hasOwnProperty('uid')) {
      dir.setUid(config.uid);
    }
    if (config.hasOwnProperty('gid')) {
      dir.setGid(config.gid);
    }
    if (config.hasOwnProperty('items')) {
      for (var name in config.items) {
        populate(dir, name, config.items[name]);
      }
    }
    if (config.hasOwnProperty('atime')) {
      dir.setATime(config.atime);
    }
    if (config.hasOwnProperty('ctime')) {
      dir.setCTime(config.ctime);
    }
    if (config.hasOwnProperty('mtime')) {
      dir.setMTime(config.mtime);
    }
    if (config.hasOwnProperty('birthtime')) {
      dir.setBirthtime(config.birthtime);
    }
    return dir;
  };
}
```
- example usage
```shell
...
       file2: new Buffer([1, 2, 3, 4])
     }
   }
 }
});
'''

To create a directory with additional properties (owner, permissions, atime, etc.), use the ['mock.directory()'](mockdirectoryproperties
) function described below.

### <a id='mockdirectoryproperties'>'mock.directory(properties)'</a>

Create a factory for new directories.  Supported properties:

* **mode** - 'number' Directory mode (permission and sticky bits).  Defaults to '0777'.
* **uid** - 'number' The user id.  Defaults to 'process.getuid()'.
...
```

#### <a name="apidoc.element.mock-fs.filesystem.file"></a>[function <span class="apidocSignatureSpan">mock-fs.filesystem.</span>file (config)](#apidoc.element.mock-fs.filesystem.file)
- description and source-code
```javascript
file = function (config) {
  config = config || {};
  return function() {
    var file = new File();
    if (config.hasOwnProperty('content')) {
      file.setContent(config.content);
    }
    if (config.hasOwnProperty('mode')) {
      file.setMode(config.mode);
    } else {
      file.setMode(438); // 0666
    }
    if (config.hasOwnProperty('uid')) {
      file.setUid(config.uid);
    }
    if (config.hasOwnProperty('gid')) {
      file.setGid(config.gid);
    }
    if (config.hasOwnProperty('atime')) {
      file.setATime(config.atime);
    }
    if (config.hasOwnProperty('ctime')) {
      file.setCTime(config.ctime);
    }
    if (config.hasOwnProperty('mtime')) {
      file.setMTime(config.mtime);
    }
    if (config.hasOwnProperty('birthtime')) {
      file.setBirthtime(config.birthtime);
    }
    return file;
  };
}
```
- example usage
```shell
...
When 'config' property values are a 'string' or 'Buffer', a file is created with the provided content.  For example, the following
 configuration creates a single file with string content (in addition to the two default directories).
'''js
mock({
 'path/to/file.txt': 'file content here'
});
'''

To create a file with additional properties (owner, permissions, atime, etc.), use the ['mock.file()'](#mockfileproperties) function
 described below.

### <a id='mockfileproperties'>'mock.file(properties)'</a>

Create a factory for new files.  Supported properties:

* **content** - 'string|Buffer' File contents.
* **mode** - 'number' File mode (permission and sticky bits).  Defaults to '0666'.
...
```

#### <a name="apidoc.element.mock-fs.filesystem.getPathParts"></a>[function <span class="apidocSignatureSpan">mock-fs.filesystem.</span>getPathParts (filepath)](#apidoc.element.mock-fs.filesystem.getPathParts)
- description and source-code
```javascript
function getPathParts(filepath) {
  var parts = path._makeLong(path.resolve(filepath)).split(path.sep);
  parts.shift();
  if (isWindows) {
    // parts currently looks like ['', '?', 'c:', ...]
    parts.shift();
    var q = parts.shift(); // should be '?'
    var base = '\\\\' + q + '\\' + parts.shift().toLowerCase();
    parts.unshift(base);
  }
  if (parts[parts.length - 1] === '') {
    parts.pop();
  }
  return parts;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mock-fs.filesystem.symlink"></a>[function <span class="apidocSignatureSpan">mock-fs.filesystem.</span>symlink (config)](#apidoc.element.mock-fs.filesystem.symlink)
- description and source-code
```javascript
symlink = function (config) {
  config = config || {};
  return function() {
    var link = new SymbolicLink();
    if (config.hasOwnProperty('mode')) {
      link.setMode(config.mode);
    } else {
      link.setMode(438); // 0666
    }
    if (config.hasOwnProperty('uid')) {
      link.setUid(config.uid);
    }
    if (config.hasOwnProperty('gid')) {
      link.setGid(config.gid);
    }
    if (config.hasOwnProperty('path')) {
      link.setPath(config.path);
    } else {
      throw new Error('Missing "path" property');
    }
    if (config.hasOwnProperty('atime')) {
      link.setATime(config.atime);
    }
    if (config.hasOwnProperty('ctime')) {
      link.setCTime(config.ctime);
    }
    if (config.hasOwnProperty('mtime')) {
      link.setMTime(config.mtime);
    }
    if (config.hasOwnProperty('birthtime')) {
      link.setBirthtime(config.birthtime);
    }
    return link;
  };
}
```
- example usage
```shell
...
});
'''

Note that if you want to create a directory with the default properties, you can provide an 'Object' directly instead of calling
 'mock.directory()'.

### Creating symlinks

Using a 'string' or a 'Buffer' is a shortcut for creating files with default properties.  Using an 'Object' is a shortcut for creating
 a directory with default properties.  There is no shortcut for creating symlinks.  To create a symlink, you need to call the ['
mock.symlink()'](#mocksymlinkproperties) function described below.

### <a id='mocksymlinkproperties'>'mock.symlink(properties)'</a>

Create a factory for new symlinks.  Supported properties:

* **path** - 'string' Path to the source (required).
* **mode** - 'number' Symlink mode (permission and sticky bits).  Defaults to '0666'.
...
```



# <a name="apidoc.module.mock-fs.filesystem.prototype"></a>[module mock-fs.filesystem.prototype](#apidoc.module.mock-fs.filesystem.prototype)

#### <a name="apidoc.element.mock-fs.filesystem.prototype.getItem"></a>[function <span class="apidocSignatureSpan">mock-fs.filesystem.prototype.</span>getItem (filepath)](#apidoc.element.mock-fs.filesystem.prototype.getItem)
- description and source-code
```javascript
getItem = function (filepath) {
  var parts = getPathParts(filepath);
  var currentParts = getPathParts(process.cwd());
  var item = this._root;
  var itemPath = '/';
  var name;
  for (var i = 0, ii = parts.length; i < ii; ++i) {
    name = parts[i];
    while (item instanceof SymbolicLink) {
      // Symbolic link being traversed as a directory --- If link targets
      // another symbolic link, resolve target's path relative to the original
      // link's target, otherwise relative to the current item.
      itemPath = path.resolve(path.dirname(itemPath), item.getPath());
      item = this.getItem(itemPath);
    }
    if (item) {
      if (item instanceof Directory && name !== currentParts[i]) {
        // make sure traversal is allowed
        if (!item.canExecute()) {
          throw new FSError('EACCES', filepath);
        }
      }
      item = item.getItem(name);
    }
    if (!item) {
      break;
    }
    itemPath = path.resolve(itemPath, name);
  }
  return item;
}
```
- example usage
```shell
...
var item = this._system.getRoot();
var itemPath = '/';
var name, i, ii;
for (i = 0, ii = parts.length; i < ii; ++i) {
  name = parts[i];
  while (item instanceof SymbolicLink) {
    itemPath = path.resolve(path.dirname(itemPath), item.getPath());
    item = this._system.getItem(itemPath);
  }
  if (!item) {
    throw new FSError('ENOENT', filepath);
  }
  if (item instanceof Directory) {
    itemPath = path.resolve(itemPath, name);
    item = item.getItem(name);
...
```

#### <a name="apidoc.element.mock-fs.filesystem.prototype.getRoot"></a>[function <span class="apidocSignatureSpan">mock-fs.filesystem.prototype.</span>getRoot ()](#apidoc.element.mock-fs.filesystem.prototype.getRoot)
- description and source-code
```javascript
getRoot = function () {
  return this._root;
}
```
- example usage
```shell
...
  return maybeCallback(callback, this, function() {
var realPath;
if (Buffer.isBuffer(filepath)) {
  filepath = filepath.toString();
}
var resolved = path.resolve(filepath);
var parts = getPathParts(resolved);
var item = this._system.getRoot();
var itemPath = '/';
var name, i, ii;
for (i = 0, ii = parts.length; i < ii; ++i) {
  name = parts[i];
  while (item instanceof SymbolicLink) {
    itemPath = path.resolve(path.dirname(itemPath), item.getPath());
    item = this._system.getItem(itemPath);
...
```



# <a name="apidoc.module.mock-fs.item"></a>[module mock-fs.item](#apidoc.module.mock-fs.item)

#### <a name="apidoc.element.mock-fs.item.item"></a>[function <span class="apidocSignatureSpan">mock-fs.</span>item ()](#apidoc.element.mock-fs.item.item)
- description and source-code
```javascript
function Item() {

  var now = Date.now();

<span class="apidocCodeCommentSpan">  /**
   * Access time.
   * @type {Date}
   */
</span>  this._atime = new Date(now);

  /**
   * Change time.
   * @type {Date}
   */
  this._ctime = new Date(now);

  /**
   * Birth time.
   * @type {Date}
   */
  this._birthtime = new Date(now);

  /**
   * Modification time.
   * @type {Date}
   */
  this._mtime = new Date(now);

  /**
   * Permissions.
   */
  this._mode = 438; // 0666

  /**
   * User id.
   * @type {number}
   */
  this._uid = getUid();

  /**
   * Group id.
   * @type {number}
   */
  this._gid = getGid();

  /**
   * Item number.
   * @type {number}
   */
  this._id = ++counter;

  /**
   * Number of links to this item.
   */
  this.links = 0;

}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mock-fs.item.prototype"></a>[module mock-fs.item.prototype](#apidoc.module.mock-fs.item.prototype)

#### <a name="apidoc.element.mock-fs.item.prototype.canExecute"></a>[function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>canExecute ()](#apidoc.element.mock-fs.item.prototype.canExecute)
- description and source-code
```javascript
canExecute = function () {
  var uid = getUid();
  var gid = getGid();
  var can = false;
  if (uid === 0) {
    can = true;
  } else if (uid === this._uid) {
    can = (permissions.USER_EXEC & this._mode) === permissions.USER_EXEC;
  } else if (gid === this._gid) {
    can = (permissions.GROUP_EXEC & this._mode) === permissions.GROUP_EXEC;
  } else {
    can = (permissions.OTHER_EXEC & this._mode) === permissions.OTHER_EXEC;
  }
  return can;
}
```
- example usage
```shell
...
  // link's target, otherwise relative to the current item.
  itemPath = path.resolve(path.dirname(itemPath), item.getPath());
  item = this.getItem(itemPath);
}
if (item) {
  if (item instanceof Directory && name !== currentParts[i]) {
    // make sure traversal is allowed
    if (!item.canExecute()) {
      throw new FSError('EACCES', filepath);
    }
  }
  item = item.getItem(name);
}
if (!item) {
  break;
...
```

#### <a name="apidoc.element.mock-fs.item.prototype.canRead"></a>[function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>canRead ()](#apidoc.element.mock-fs.item.prototype.canRead)
- description and source-code
```javascript
canRead = function () {
  var uid = getUid();
  var gid = getGid();
  var can = false;
  if (uid === 0) {
    can = true;
  } else if (uid === this._uid) {
    can = (permissions.USER_READ & this._mode) === permissions.USER_READ;
  } else if (gid === this._gid) {
    can = (permissions.GROUP_READ & this._mode) === permissions.GROUP_READ;
  } else {
    can = (permissions.OTHER_READ & this._mode) === permissions.OTHER_READ;
  }
  return can;
}
```
- example usage
```shell
...
  }
  parent.addItem(path.basename(pathname), item);
}
if (descriptor.isRead()) {
  if (!item) {
    throw new FSError('ENOENT', pathname);
  }
  if (!item.canRead()) {
    throw new FSError('EACCES', pathname);
  }
}
if (descriptor.isWrite() && !item.canWrite()) {
  throw new FSError('EACCES', pathname);
}
if (descriptor.isTruncate()) {
...
```

#### <a name="apidoc.element.mock-fs.item.prototype.canWrite"></a>[function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>canWrite ()](#apidoc.element.mock-fs.item.prototype.canWrite)
- description and source-code
```javascript
canWrite = function () {
  var uid = getUid();
  var gid = getGid();
  var can = false;
  if (uid === 0) {
    can = true;
  } else if (uid === this._uid) {
    can = (permissions.USER_WRITE & this._mode) === permissions.USER_WRITE;
  } else if (gid === this._gid) {
    can = (permissions.GROUP_WRITE & this._mode) === permissions.GROUP_WRITE;
  } else {
    can = (permissions.OTHER_WRITE & this._mode) === permissions.OTHER_WRITE;
  }
  return can;
}
```
- example usage
```shell
...
  if (!item) {
    throw new FSError('ENOENT', pathname);
  }
  if (!item.canRead()) {
    throw new FSError('EACCES', pathname);
  }
}
if (descriptor.isWrite() && !item.canWrite()) {
  throw new FSError('EACCES', pathname);
}
if (descriptor.isTruncate()) {
  item.setContent('');
}
if (descriptor.isTruncate() || descriptor.isAppend()) {
  descriptor.setPosition(item.getContent().length);
...
```

#### <a name="apidoc.element.mock-fs.item.prototype.getATime"></a>[function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>getATime ()](#apidoc.element.mock-fs.item.prototype.getATime)
- description and source-code
```javascript
getATime = function () {
  return this._atime;
}
```
- example usage
```shell
...
    dev: 8675309,
    nlink: this.links,
    uid: this.getUid(),
    gid: this.getGid(),
    rdev: 0,
    blksize: 4096,
    ino: this._id,
    atime: this.getATime(),
    mtime: this.getMTime(),
    ctime: this.getCTime(),
    birthtime: this.getBirthtime()
  };
};
...
```

#### <a name="apidoc.element.mock-fs.item.prototype.getBirthtime"></a>[function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>getBirthtime ()](#apidoc.element.mock-fs.item.prototype.getBirthtime)
- description and source-code
```javascript
getBirthtime = function () {
  return this._birthtime;
}
```
- example usage
```shell
...
   gid: this.getGid(),
   rdev: 0,
   blksize: 4096,
   ino: this._id,
   atime: this.getATime(),
   mtime: this.getMTime(),
   ctime: this.getCTime(),
   birthtime: this.getBirthtime()
 };
};


/**
* Get the item's string representation.
* @return {string} String representation.
...
```

#### <a name="apidoc.element.mock-fs.item.prototype.getCTime"></a>[function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>getCTime ()](#apidoc.element.mock-fs.item.prototype.getCTime)
- description and source-code
```javascript
getCTime = function () {
  return this._ctime;
}
```
- example usage
```shell
...
   uid: this.getUid(),
   gid: this.getGid(),
   rdev: 0,
   blksize: 4096,
   ino: this._id,
   atime: this.getATime(),
   mtime: this.getMTime(),
   ctime: this.getCTime(),
   birthtime: this.getBirthtime()
 };
};


/**
* Get the item's string representation.
...
```

#### <a name="apidoc.element.mock-fs.item.prototype.getGid"></a>[function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>getGid ()](#apidoc.element.mock-fs.item.prototype.getGid)
- description and source-code
```javascript
getGid = function () {
  return this._gid;
}
```
- example usage
```shell
...
}
if (mode && process.getuid && process.getgid) {
  var itemMode = item.getMode();
  if (item.getUid() === process.getuid()) {
    if ((itemMode & (mode * 64)) !== mode * 64) {
      throw new FSError('EACCES', filepath);
    }
  } else if (item.getGid() === process.getgid()) {
    if ((itemMode & (mode * 8)) !== mode * 8) {
      throw new FSError('EACCES', filepath);
    }
  } else {
    if ((itemMode & mode) !== mode) {
      throw new FSError('EACCES', filepath);
    }
...
```

#### <a name="apidoc.element.mock-fs.item.prototype.getMTime"></a>[function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>getMTime ()](#apidoc.element.mock-fs.item.prototype.getMTime)
- description and source-code
```javascript
getMTime = function () {
  return this._mtime;
}
```
- example usage
```shell
...
    nlink: this.links,
    uid: this.getUid(),
    gid: this.getGid(),
    rdev: 0,
    blksize: 4096,
    ino: this._id,
    atime: this.getATime(),
    mtime: this.getMTime(),
    ctime: this.getCTime(),
    birthtime: this.getBirthtime()
  };
};


/**
...
```

#### <a name="apidoc.element.mock-fs.item.prototype.getMode"></a>[function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>getMode ()](#apidoc.element.mock-fs.item.prototype.getMode)
- description and source-code
```javascript
getMode = function () {
  return this._mode;
}
```
- example usage
```shell
...
Binding.prototype.access = function(filepath, mode, callback) {
maybeCallback(callback, this, function() {
  var item = this._system.getItem(filepath);
  if (!item) {
    throw new FSError('ENOENT', filepath);
  }
  if (mode && process.getuid && process.getgid) {
    var itemMode = item.getMode();
    if (item.getUid() === process.getuid()) {
      if ((itemMode & (mode * 64)) !== mode * 64) {
        throw new FSError('EACCES', filepath);
      }
    } else if (item.getGid() === process.getgid()) {
      if ((itemMode & (mode * 8)) !== mode * 8) {
        throw new FSError('EACCES', filepath);
...
```

#### <a name="apidoc.element.mock-fs.item.prototype.getStats"></a>[function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>getStats ()](#apidoc.element.mock-fs.item.prototype.getStats)
- description and source-code
```javascript
getStats = function () {
  return {
    dev: 8675309,
    nlink: this.links,
    uid: this.getUid(),
    gid: this.getGid(),
    rdev: 0,
    blksize: 4096,
    ino: this._id,
    atime: this.getATime(),
    mtime: this.getMTime(),
    ctime: this.getCTime(),
    birthtime: this.getBirthtime()
  };
}
```
- example usage
```shell
...
if (item instanceof SymbolicLink) {
  item = this._system.getItem(
      path.resolve(path.dirname(filepath), item.getPath()));
}
if (!item) {
  throw new FSError('ENOENT', filepath);
}
var stats = item.getStats();

// In Node 7.7.0+, binding.stat accepts a Float64Array as the second argument,
// which should be filled with stat values.
// In prior versions of Node, binding.stat simply returns a Stats instance.
if (callback instanceof Float64Array) {
  fillStatsArray(stats, callback);
} else {
...
```

#### <a name="apidoc.element.mock-fs.item.prototype.getUid"></a>[function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>getUid ()](#apidoc.element.mock-fs.item.prototype.getUid)
- description and source-code
```javascript
getUid = function () {
  return this._uid;
}
```
- example usage
```shell
...
  maybeCallback(callback, this, function() {
var item = this._system.getItem(filepath);
if (!item) {
  throw new FSError('ENOENT', filepath);
}
if (mode && process.getuid && process.getgid) {
  var itemMode = item.getMode();
  if (item.getUid() === process.getuid()) {
    if ((itemMode & (mode * 64)) !== mode * 64) {
      throw new FSError('EACCES', filepath);
    }
  } else if (item.getGid() === process.getgid()) {
    if ((itemMode & (mode * 8)) !== mode * 8) {
      throw new FSError('EACCES', filepath);
    }
...
```

#### <a name="apidoc.element.mock-fs.item.prototype.setATime"></a>[function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>setATime (atime)](#apidoc.element.mock-fs.item.prototype.setATime)
- description and source-code
```javascript
setATime = function (atime) {
  this._atime = atime;
}
```
- example usage
```shell
...
*/
Binding.prototype.utimes = function(pathname, atime, mtime, callback) {
 maybeCallback(callback, this, function() {
   var item = this._system.getItem(pathname);
   if (!item) {
     throw new FSError('ENOENT', pathname);
   }
   item.setATime(new Date(atime * 1000));
   item.setMTime(new Date(mtime * 1000));
 });
};


/**
* Update timestamps.
...
```

#### <a name="apidoc.element.mock-fs.item.prototype.setBirthtime"></a>[function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>setBirthtime (birthtime)](#apidoc.element.mock-fs.item.prototype.setBirthtime)
- description and source-code
```javascript
setBirthtime = function (birthtime) {
  this._birthtime = birthtime;
}
```
- example usage
```shell
...
    if (config.hasOwnProperty('ctime')) {
      file.setCTime(config.ctime);
    }
    if (config.hasOwnProperty('mtime')) {
      file.setMTime(config.mtime);
    }
    if (config.hasOwnProperty('birthtime')) {
      file.setBirthtime(config.birthtime);
    }
    return file;
  };
};


/**
...
```

#### <a name="apidoc.element.mock-fs.item.prototype.setCTime"></a>[function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>setCTime (ctime)](#apidoc.element.mock-fs.item.prototype.setCTime)
- description and source-code
```javascript
setCTime = function (ctime) {
  this._ctime = ctime;
}
```
- example usage
```shell
...
 if (typeof content === 'string') {
   content = new Buffer(content);
 } else if (!Buffer.isBuffer(content)) {
   throw new Error('File content must be a string or buffer');
 }
 this._content = content;
 var now = Date.now();
 this.setCTime(new Date(now));
 this.setMTime(new Date(now));
};


/**
* Get file stats.
* @return {Object} Stats properties.
...
```

#### <a name="apidoc.element.mock-fs.item.prototype.setGid"></a>[function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>setGid (gid)](#apidoc.element.mock-fs.item.prototype.setGid)
- description and source-code
```javascript
setGid = function (gid) {
  this.setCTime(new Date());
  this._gid = gid;
}
```
- example usage
```shell
...
Binding.prototype.chown = function(pathname, uid, gid, callback) {
 maybeCallback(callback, this, function() {
   var item = this._system.getItem(pathname);
   if (!item) {
     throw new FSError('ENOENT', pathname);
   }
   item.setUid(uid);
   item.setGid(gid);
 });
};


/**
* Change user and group owner.
* @param {number} fd File descriptor.
...
```

#### <a name="apidoc.element.mock-fs.item.prototype.setMTime"></a>[function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>setMTime (mtime)](#apidoc.element.mock-fs.item.prototype.setMTime)
- description and source-code
```javascript
setMTime = function (mtime) {
  this._mtime = mtime;
}
```
- example usage
```shell
...
Binding.prototype.utimes = function(pathname, atime, mtime, callback) {
 maybeCallback(callback, this, function() {
   var item = this._system.getItem(pathname);
   if (!item) {
     throw new FSError('ENOENT', pathname);
   }
   item.setATime(new Date(atime * 1000));
   item.setMTime(new Date(mtime * 1000));
 });
};


/**
* Update timestamps.
* @param {number} fd File descriptor.
...
```

#### <a name="apidoc.element.mock-fs.item.prototype.setMode"></a>[function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>setMode (mode)](#apidoc.element.mock-fs.item.prototype.setMode)
- description and source-code
```javascript
setMode = function (mode) {
  this.setCTime(new Date());
  this._mode = mode;
}
```
- example usage
```shell
...
    throw new FSError('ENOENT', pathname);
  }
  if (!(parent instanceof Directory)) {
    throw new FSError('ENOTDIR', pathname);
  }
  item = new File();
  if (mode) {
    item.setMode(mode);
  }
  parent.addItem(path.basename(pathname), item);
}
if (descriptor.isRead()) {
  if (!item) {
    throw new FSError('ENOENT', pathname);
  }
...
```

#### <a name="apidoc.element.mock-fs.item.prototype.setUid"></a>[function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>setUid (uid)](#apidoc.element.mock-fs.item.prototype.setUid)
- description and source-code
```javascript
setUid = function (uid) {
  this.setCTime(new Date());
  this._uid = uid;
}
```
- example usage
```shell
...
*/
Binding.prototype.chown = function(pathname, uid, gid, callback) {
 maybeCallback(callback, this, function() {
   var item = this._system.getItem(pathname);
   if (!item) {
     throw new FSError('ENOENT', pathname);
   }
   item.setUid(uid);
   item.setGid(gid);
 });
};


/**
* Change user and group owner.
...
```

#### <a name="apidoc.element.mock-fs.item.prototype.toString"></a>[function <span class="apidocSignatureSpan">mock-fs.item.prototype.</span>toString ()](#apidoc.element.mock-fs.item.prototype.toString)
- description and source-code
```javascript
toString = function () {
  return '[' + this.constructor.name + ']';
}
```
- example usage
```shell
...
 * @param {string} encoding The encoding for the return.
 * @return {string|Buffer} The real path.
 */
Binding.prototype.realpath = function(filepath, encoding, callback) {
return maybeCallback(callback, this, function() {
  var realPath;
  if (Buffer.isBuffer(filepath)) {
    filepath = filepath.toString();
  }
  var resolved = path.resolve(filepath);
  var parts = getPathParts(resolved);
  var item = this._system.getRoot();
  var itemPath = '/';
  var name, i, ii;
  for (i = 0, ii = parts.length; i < ii; ++i) {
...
```



# <a name="apidoc.module.mock-fs.symlink"></a>[module mock-fs.symlink](#apidoc.module.mock-fs.symlink)

#### <a name="apidoc.element.mock-fs.symlink.symlink"></a>[function <span class="apidocSignatureSpan">mock-fs.</span>symlink ()](#apidoc.element.mock-fs.symlink.symlink)
- description and source-code
```javascript
function SymbolicLink() {
  Item.call(this);

<span class="apidocCodeCommentSpan">  /**
   * Relative path to source.
   * @type {string}
   */
</span>  this._path = undefined;

}
```
- example usage
```shell
...
});
'''

Note that if you want to create a directory with the default properties, you can provide an 'Object' directly instead of calling
 'mock.directory()'.

### Creating symlinks

Using a 'string' or a 'Buffer' is a shortcut for creating files with default properties.  Using an 'Object' is a shortcut for creating
 a directory with default properties.  There is no shortcut for creating symlinks.  To create a symlink, you need to call the ['
mock.symlink()'](#mocksymlinkproperties) function described below.

### <a id='mocksymlinkproperties'>'mock.symlink(properties)'</a>

Create a factory for new symlinks.  Supported properties:

* **path** - 'string' Path to the source (required).
* **mode** - 'number' Symlink mode (permission and sticky bits).  Defaults to '0666'.
...
```

#### <a name="apidoc.element.mock-fs.symlink.super_"></a>[function <span class="apidocSignatureSpan">mock-fs.symlink.</span>super_ ()](#apidoc.element.mock-fs.symlink.super_)
- description and source-code
```javascript
function Item() {

  var now = Date.now();

<span class="apidocCodeCommentSpan">  /**
   * Access time.
   * @type {Date}
   */
</span>  this._atime = new Date(now);

  /**
   * Change time.
   * @type {Date}
   */
  this._ctime = new Date(now);

  /**
   * Birth time.
   * @type {Date}
   */
  this._birthtime = new Date(now);

  /**
   * Modification time.
   * @type {Date}
   */
  this._mtime = new Date(now);

  /**
   * Permissions.
   */
  this._mode = 438; // 0666

  /**
   * User id.
   * @type {number}
   */
  this._uid = getUid();

  /**
   * Group id.
   * @type {number}
   */
  this._gid = getGid();

  /**
   * Item number.
   * @type {number}
   */
  this._id = ++counter;

  /**
   * Number of links to this item.
   */
  this.links = 0;

}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mock-fs.symlink.prototype"></a>[module mock-fs.symlink.prototype](#apidoc.module.mock-fs.symlink.prototype)

#### <a name="apidoc.element.mock-fs.symlink.prototype.getPath"></a>[function <span class="apidocSignatureSpan">mock-fs.symlink.prototype.</span>getPath ()](#apidoc.element.mock-fs.symlink.prototype.getPath)
- description and source-code
```javascript
getPath = function () {
  return this._path;
}
```
- example usage
```shell
...
var parts = getPathParts(resolved);
var item = this._system.getRoot();
var itemPath = '/';
var name, i, ii;
for (i = 0, ii = parts.length; i < ii; ++i) {
  name = parts[i];
  while (item instanceof SymbolicLink) {
    itemPath = path.resolve(path.dirname(itemPath), item.getPath());
    item = this._system.getItem(itemPath);
  }
  if (!item) {
    throw new FSError('ENOENT', filepath);
  }
  if (item instanceof Directory) {
    itemPath = path.resolve(itemPath, name);
...
```

#### <a name="apidoc.element.mock-fs.symlink.prototype.getStats"></a>[function <span class="apidocSignatureSpan">mock-fs.symlink.prototype.</span>getStats ()](#apidoc.element.mock-fs.symlink.prototype.getStats)
- description and source-code
```javascript
getStats = function () {
  var size = this._path.length;
  var stats = Item.prototype.getStats.call(this);
  stats.mode = this.getMode() | constants.S_IFLNK;
  stats.size = size;
  stats.blocks = Math.ceil(size / 512);
  return stats;
}
```
- example usage
```shell
...
if (item instanceof SymbolicLink) {
  item = this._system.getItem(
      path.resolve(path.dirname(filepath), item.getPath()));
}
if (!item) {
  throw new FSError('ENOENT', filepath);
}
var stats = item.getStats();

// In Node 7.7.0+, binding.stat accepts a Float64Array as the second argument,
// which should be filled with stat values.
// In prior versions of Node, binding.stat simply returns a Stats instance.
if (callback instanceof Float64Array) {
  fillStatsArray(stats, callback);
} else {
...
```

#### <a name="apidoc.element.mock-fs.symlink.prototype.setPath"></a>[function <span class="apidocSignatureSpan">mock-fs.symlink.prototype.</span>setPath (pathname)](#apidoc.element.mock-fs.symlink.prototype.setPath)
- description and source-code
```javascript
setPath = function (pathname) {
  this._path = pathname;
}
```
- example usage
```shell
...
   if (!parent) {
     throw new FSError('ENOENT', destPath);
   }
   if (!(parent instanceof Directory)) {
     throw new FSError('ENOTDIR', destPath);
   }
   var link = new SymbolicLink();
   link.setPath(srcPath);
   parent.addItem(path.basename(destPath), link);
 });
};


/**
* Read the contents of a symbolic link.
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
