# posix-tools

A collection of pure (almost) JavaScript POSIX-like tools.

### goal
The primary goal of this project is to build a comprehensive list of POSIX-like tools written in JavaScript. In no way do I claim any of these to be POSIX compliant nor have plans to be certified to say so.

The secondary goal is to fill in the blanks with pure JavaScript, platform agnostic POSIX-like tools. In other words, the same interface can be ran through Node.js/io.js on Windows/OSX/Linux as well as independently in a web browser.

### example

Please see [posix-cat](https://github.com/shama/posix-cat) for an example agnostic POSIX-like JavaScript tool.

```shell
npm install posix-cat
```

Then in your `package.json` you can use `cat`:

```json
{
  "name": "myapp",
  "version": "1.0.0",
  "scripts": {
    "build": "cat one.js two.js"
  },
  "dependencies": {
    "posix-cat": "^1.1.0"
  }
}
```

and `npm run build` should run the same on Windows/OSX/Linux.

The API will also work in a web browser by supplying a Node.js/io.js compatible file system interface:

```js
var cat = require('posix-cat')({
  // File inputs go in through a _ array
  _: ['one.js', 'two.js'],
  fs: {
    createReadStream: function(filename) { /* return a read file stream */ }
  },
})
cat.on('data', function(data) {
  console.log(data.toString())
})
```

### please contribute!
If you know of a tool in JavaScript that works similar to a POSIX utility, please add it to this list!

---

> Server: Will only run on the server side.
> Alias: Will exec the OS's binary tool.

## [admin](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/admin.html)

## [alias](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/alias.html)

## [ar](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/ar.html)

## [asa](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/asa.html)

## [at](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/at.html)

## [awk](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/awk.html)

## [basename](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/basename.html)
* [path.basename](https://iojs.org/api/path.html#path_path_basename_p_ext)

## [batch](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/batch.html)

## [bc](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/bc.html)

## [bg](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/bg.html)

## [c99](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/c99.html)

## [cal](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/cal.html)

## [cat](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/cat.html)
* [posix-cat](https://www.npmjs.com/package/posix-cat)

## [cd](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/cd.html)
* Server
  + [process.chdir](https://iojs.org/api/process.html#process_process_chdir_directory)

## [cflow](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/cflow.html)

## [chgrp](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/chgrp.html)

## [chmod](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/chmod.html)
* Server
  + [chmod](https://www.npmjs.com/package/chmod)
  + [fs.chmod](https://iojs.org/api/fs.html#fs_fs_chmod_path_mode_callback)

## [chown](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/chown.html)
* Server
  + [chownr](https://www.npmjs.com/package/chownr)
  + [fs.chown](https://iojs.org/api/fs.html#fs_fs_chown_path_uid_gid_callback)

## [cksum](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/cksum.html)

## [cmp](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/cmp.html)

## [comm](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/comm.html)

## [command](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/command.html)

## [compress](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/compress.html)

## [cp](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/cp.html)
* Server
  + [cpr](https://www.npmjs.com/package/cpr)
  + [cpy](https://www.npmjs.com/package/cpy)

## [crontab](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/crontab.html)
* `setTimeout`

## [csplit](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/csplit.html)

## [ctags](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/ctags.html)

## [cut](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/cut.html)

## [cxref](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/cxref.html)

## [date](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/date.html)

## [dd](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/dd.html)

## [delta](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/delta.html)

## [df](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/df.html)
* Alias
  + [df](https://www.npmjs.com/package/df)

## [diff](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/diff.html)

## [dirname](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/dirname.html)
* [path.dirname](https://iojs.org/api/path.html#path_path_dirname_p)

## [du](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/du.html)

## [echo](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/echo.html)
* [posix-echo](https://www.npmjs.com/package/posix-echo)

## [ed](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/ed.html)

## [env](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/env.html)

## [ex](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/ex.html)

## [expand](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/expand.html)
* [posix-expand](https://www.npmjs.com/package/posix-expand)

## [expr](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/expr.html)

## [false](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/false.html)
* `false`
* [false](https://www.npmjs.com/package/false)

## [fc](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/fc.html)

## [fg](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/fg.html)

## [file](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/file.html)

## [find](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/find.html)

## [fold](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/fold.html)

## [fort77](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/fort77.html)

## [fuser](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/fuser.html)

## [gencat](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/gencat.html)

## [get](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/get.html)

## [getconf](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/getconf.html)

## [getopts](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/getopts.html)

## [grep](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/grep.html)
* Alias
  + [grep1](https://www.npmjs.com/package/grep1)

## [hash](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/hash.html)

## [head](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/head.html)
* [posix-head](https://www.npmjs.com/package/posix-head)

## [iconv](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/iconv.html)

## [id](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/id.html)

## [ipcrm](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/ipcrm.html)

## [ipcs](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/ipcs.html)

## [jobs](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/jobs.html)

## [join](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/join.html)

## [kill](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/kill.html)

## [lex](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/lex.html)

## [link](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/link.html)

## [ln](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/ln.html)
* Server
  + [lnfs](https://www.npmjs.com/package/lnfs)

## [locale](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/locale.html)

## [localedef](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/localedef.html)

## [logger](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/logger.html)

## [logname](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/logname.html)

## [lp](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/lp.html)

## [ls](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/ls.html)
* Server
  + [readdirp](https://www.npmjs.com/package/readdirp)
  + [fs.readdir](http://nodejs.org/api/fs.html#fs_fs_readdir_path_callback)
  + [ls-stream](https://www.npmjs.com/package/ls-stream)

## [m4](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/m4.html)

## [mailx](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/malix.html)

## [make](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/make.html)

## [man](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/man.html)

## [mesg](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/mesg.html)

## [mkdir](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/mkdir.html)
* Server
  + [mkdirp](https://www.npmjs.com/package/mkdirp)
  + [fs.mkdir](https://iojs.org/api/fs.html#fs_fs_mkdir_path_mode_callback)

## [mkfifo](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/mkfifo.html)

## [more](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/more.html)

## [mv](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/mv.html)
* Server
  + [mv](https://www.npmjs.com/package/mv)
  + [fs.rename](http://nodejs.org/api/fs.html#fs_fs_rename_oldpath_newpath_callback)

## [newgrp](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/newgrp.html)

## [nice](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/nice.html)

## [nl](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/nl.html)

## [nm](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/nm.html)

## [nohup](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/nohup.html)

## [od](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/od.html)

## [paste](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/paste.html)

## [patch](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/patch.html)

## [pathchk](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/pathchk.html)

## [pax](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/pax.html)

## [pr](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/pr.html)

## [printf](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/printf.html)
* [printf](https://www.npmjs.com/package/printf)

## [prs](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/prs.html)

## [ps](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/ps.html)

## [pwd](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/pwd.html)

## [qalter](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/qalter.html)

## [qdel](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/qdel.html)

## [qhold](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/qhold.html)

## [qmove](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/qmove.html)

## [qmsg](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/qmsg.html)

## [qrerun](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/qrerun.html)

## [qrls](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/qrls.html)

## [qselect](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/qselect.html)

## [qsig](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/qsig.html)

## [qstat](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/qstat.html)

## [qsub](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/qsub.html)

## [read](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/read.html)

## [renice](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/renice.html)

## [rm](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/rm.html)
* Server
  + [rimraf](https://www.npmjs.com/package/rimraf)
  + [fs.unlink](https://iojs.org/api/fs.html#fs_fs_unlink_path_callback)
  + [trash](https://www.npmjs.com/package/trash)

## [rmdel](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/rmdel.html)

## [rmdir](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/rmdir.html)
* Server
  + [rimraf](https://www.npmjs.com/package/rimraf)
  + [fs.rmdir](https://iojs.org/api/fs.html#fs_fs_rmdir_path_callback)
  + [trash](https://www.npmjs.com/package/trash)

## [sact](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/sact.html)

## [sccs](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/sccs.html)

## [sed](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/sed.html)
* [sed.js](https://www.npmjs.com/package/sed.js)

## [sh](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/sh.html)

## [sleep](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/sleep.html)
* [sleep](https://www.npmjs.com/package/sleep)

## [sort](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/sort.html)
* [unix-sort](https://www.npmjs.com/package/unix-sort)

## [split](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/split.html)

## [strings](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/strings.html)

## [strip](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/strip.html)

## [stty](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/stty.html)

## [tabs](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/tabs.html)

## [tail](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/tail.html)
* Server
  + [file-tail](https://www.npmjs.com/package/file-tail)

## [talk](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/talk.html)

## [tee](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/tee.html)

## [test](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/test.html)

## [time](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/time.html)

## [touch](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/touch.html)
* [touch](https://www.npmjs.com/package/touch)

## [tput](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/tput.html)

## [tr](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/tr.html)

## [true](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/true.html)
* `true`
* [true](https://www.npmjs.com/package/true)

## [tsort](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/tsort.html)

## [tty](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/tty.html)

## [type](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/type.html)

## [ulimit](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/ulimit.html)

## [umask](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/umask.html)

## [unalias](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/unalias.html)

## [uname](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/uname.html)

## [uncompress](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/uncompress.html)

## [unexpand](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/unexpand.html)

## [unget](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/unget.html)

## [uniq](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/uniq.html)
  + [uniq-stream](https://www.npmjs.com/package/uniq-stream)

## [unlink](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/unlink.html)
* Server
  + [rimraf](https://www.npmjs.com/package/rimraf)
  + [fs.unlink](https://iojs.org/api/fs.html#fs_fs_unlink_path_callback)

## [uucp](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/uucp.html)

## [uudecode](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/uudecode.html)

## [uuencode](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/uuencode.html)

## [uustat](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/uustat.html)

## [uux](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/uux.html)

## [val](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/val.html)

## [vi](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/vi.html)

## [wait](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/wait.html)

## [wc](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/wc.html)
  + [wordcount-stream](https://www.npmjs.com/package/wordcount-stream)

## [what](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/what.html)

## [who](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/who.html)

## [write](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/write.html)

## [xargs](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/xargs.html)

## [yacc](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/yacc.html)

## [zcat](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/zcat.html)

---

## Other
* Server
  + [posix](https://www.npmjs.com/package/posix)
  + [posix-ext](https://www.npmjs.com/package/posix-ext)
  + [shelljs](https://www.npmjs.com/package/shelljs)

## Reference

* [http://pubs.opengroup.org/onlinepubs/9699919799/idx/utilities.html](http://pubs.opengroup.org/onlinepubs/9699919799/idx/utilities.html)
