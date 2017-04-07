# api documentation for  [release-it (v2.7.1)](https://github.com/webpro/release-it#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-release-it.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-release-it) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-release-it.svg)](https://travis-ci.org/npmdoc/node-npmdoc-release-it)
#### Interactive release tool for Git repositories. Increment version, commit, tag, push, build, publish to npm. Supports to build and release to a distribution/component repository.

[![NPM](https://nodei.co/npm/release-it.png?downloads=true)](https://www.npmjs.com/package/release-it)

[![apidoc](https://npmdoc.github.io/node-npmdoc-release-it/build/screenCapture.buildNpmdoc.browser.%2Fhome%2Ftravis%2Fbuild%2Fnpmdoc%2Fnode-npmdoc-release-it%2Ftmp%2Fbuild%2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-release-it/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-release-it/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-release-it/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Lars Kappert",
        "email": "lars@webpro.nl"
    },
    "bin": {
        "release-it": "./bin/release.js"
    },
    "bugs": {
        "url": "https://github.com/webpro/release-it/issues"
    },
    "dependencies": {
        "chalk": "1.1.3",
        "github": "9.1.0",
        "glob": "7.1.1",
        "graceful-fs": "4.1.11",
        "inquirer": "3.0.6",
        "lodash": "4.17.4",
        "minimist": "1.2.0",
        "mkdirp": "0.5.1",
        "parse-repo": "1.0.1",
        "semver": "5.3.0",
        "shelljs": "0.7.6",
        "when": "3.7.8"
    },
    "description": "Interactive release tool for Git repositories. Increment version, commit, tag, push, build, publish to npm. Supports to build and release to a distribution/component repository.",
    "devDependencies": {
        "eslint": "^3.17.0"
    },
    "directories": {},
    "dist": {
        "shasum": "dcd87544c45d32bb74e86ebceab4e152fcc87773",
        "tarball": "https://registry.npmjs.org/release-it/-/release-it-2.7.1.tgz"
    },
    "engines": {
        "node": ">=4"
    },
    "gitHead": "5997b7a1b1a0915bdad3a2c395a9e9b561e82ce7",
    "homepage": "https://github.com/webpro/release-it#readme",
    "keywords": [
        "build",
        "commit",
        "distribution",
        "git",
        "github",
        "interactive",
        "npm",
        "publish",
        "push",
        "release",
        "repository",
        "script",
        "shell",
        "tag",
        "tool",
        "version"
    ],
    "license": "MIT",
    "main": "./lib/release.js",
    "maintainers": [
        {
            "name": "webpro",
            "email": "lars@webpro.nl"
        }
    ],
    "name": "release-it",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/webpro/release-it.git"
    },
    "scripts": {
        "lint": "eslint lib"
    },
    "version": "2.7.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module release-it](#apidoc.module.release-it)
1.  [function <span class="apidocSignatureSpan">release-it.</span>cli (args)](#apidoc.element.release-it.cli)
1.  [function <span class="apidocSignatureSpan">release-it.</span>execute (opts)](#apidoc.element.release-it.execute)
1.  object <span class="apidocSignatureSpan">release-it.</span>git
1.  object <span class="apidocSignatureSpan">release-it.</span>shell
1.  object <span class="apidocSignatureSpan">release-it.</span>tasks
1.  object <span class="apidocSignatureSpan">release-it.</span>util

#### [module release-it.git](#apidoc.module.release-it.git)
1.  [function <span class="apidocSignatureSpan">release-it.git.</span>clone (repo, dir)](#apidoc.element.release-it.git.clone)
1.  [function <span class="apidocSignatureSpan">release-it.git.</span>commit (path, message, version)](#apidoc.element.release-it.git.commit)
1.  [function <span class="apidocSignatureSpan">release-it.git.</span>getChangelog (options)](#apidoc.element.release-it.git.getChangelog)
1.  [function <span class="apidocSignatureSpan">release-it.git.</span>getGithubToken (tokenRef)](#apidoc.element.release-it.git.getGithubToken)
1.  [function <span class="apidocSignatureSpan">release-it.git.</span>getLatestTag ()](#apidoc.element.release-it.git.getLatestTag)
1.  [function <span class="apidocSignatureSpan">release-it.git.</span>getRemoteUrl ()](#apidoc.element.release-it.git.getRemoteUrl)
1.  [function <span class="apidocSignatureSpan">release-it.git.</span>hasChanges (repo)](#apidoc.element.release-it.git.hasChanges)
1.  [function <span class="apidocSignatureSpan">release-it.git.</span>isGitRepo ()](#apidoc.element.release-it.git.isGitRepo)
1.  [function <span class="apidocSignatureSpan">release-it.git.</span>isWorkingDirClean (requireCleanWorkingDir)](#apidoc.element.release-it.git.isWorkingDirClean)
1.  [function <span class="apidocSignatureSpan">release-it.git.</span>push (remoteUrl, pushUrl)](#apidoc.element.release-it.git.push)
1.  [function <span class="apidocSignatureSpan">release-it.git.</span>pushTags (version, pushUrl)](#apidoc.element.release-it.git.pushTags)
1.  [function <span class="apidocSignatureSpan">release-it.git.</span>release (options, remoteUrl, tagName)](#apidoc.element.release-it.git.release)
1.  [function <span class="apidocSignatureSpan">release-it.git.</span>stage (file)](#apidoc.element.release-it.git.stage)
1.  [function <span class="apidocSignatureSpan">release-it.git.</span>stageDir (baseDir)](#apidoc.element.release-it.git.stageDir)
1.  [function <span class="apidocSignatureSpan">release-it.git.</span>status ()](#apidoc.element.release-it.git.status)
1.  [function <span class="apidocSignatureSpan">release-it.git.</span>tag (version, tag, annotation)](#apidoc.element.release-it.git.tag)

#### [module release-it.shell](#apidoc.module.release-it.shell)
1.  [function <span class="apidocSignatureSpan">release-it.shell.</span>build (command)](#apidoc.element.release-it.shell.build)
1.  [function <span class="apidocSignatureSpan">release-it.shell.</span>bump (file, version)](#apidoc.element.release-it.shell.bump)
1.  [function <span class="apidocSignatureSpan">release-it.shell.</span>copy (files, options, target)](#apidoc.element.release-it.shell.copy)
1.  [function <span class="apidocSignatureSpan">release-it.shell.</span>mkCleanDir (dir)](#apidoc.element.release-it.shell.mkCleanDir)
1.  [function <span class="apidocSignatureSpan">release-it.shell.</span>npmPublish (path, tag)](#apidoc.element.release-it.shell.npmPublish)
1.  [function <span class="apidocSignatureSpan">release-it.shell.</span>popd ()](#apidoc.element.release-it.shell.popd)
1.  [function <span class="apidocSignatureSpan">release-it.shell.</span>pushd (path)](#apidoc.element.release-it.shell.pushd)
1.  [function <span class="apidocSignatureSpan">release-it.shell.</span>run (command, commandArgs)](#apidoc.element.release-it.shell.run)
1.  [function <span class="apidocSignatureSpan">release-it.shell.</span>runTemplateCommand (command)](#apidoc.element.release-it.shell.runTemplateCommand)

#### [module release-it.tasks](#apidoc.module.release-it.tasks)
1.  [function <span class="apidocSignatureSpan">release-it.tasks.</span>run (options)](#apidoc.element.release-it.tasks.run)

#### [module release-it.util](#apidoc.module.release-it.util)
1.  [function <span class="apidocSignatureSpan">release-it.util.</span>format (template, replacements)](#apidoc.element.release-it.util.format)
1.  [function <span class="apidocSignatureSpan">release-it.util.</span>increment (version, increment, identifier)](#apidoc.element.release-it.util.increment)
1.  [function <span class="apidocSignatureSpan">release-it.util.</span>isValidVersion (value)](#apidoc.element.release-it.util.isValidVersion)
1.  [function <span class="apidocSignatureSpan">release-it.util.</span>template (input, context)](#apidoc.element.release-it.util.template)



# <a name="apidoc.module.release-it"></a>[module release-it](#apidoc.module.release-it)

#### <a name="apidoc.element.release-it.cli"></a>[function <span class="apidocSignatureSpan">release-it.</span>cli (args)](#apidoc.element.release-it.cli)
- description and source-code
```javascript
function fromCli(args) {
  return execute(config.parseArgs(args));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.release-it.execute"></a>[function <span class="apidocSignatureSpan">release-it.</span>execute (opts)](#apidoc.element.release-it.execute)
- description and source-code
```javascript
function execute(opts) {

  config.mergeOptions(opts);

  if(config.isShowVersion) {

    cli.version();

  } else if(config.isShowHelp) {

    cli.help();

  } else {

    if(config.isForce) {
      log.warn('Using --force, I sure hope you know what you are doing.');
    }

    if(config.isDebug) {
      require('when/monitor/console');
    }

    log.debugDir(config.options);

    return tasks.run(config.options).catch(error => {

      log.error(error);

      if(config.isDebug) {
        throw error;
      }

    });
  }

  return noop;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.release-it.git"></a>[module release-it.git](#apidoc.module.release-it.git)

#### <a name="apidoc.element.release-it.git.clone"></a>[function <span class="apidocSignatureSpan">release-it.git.</span>clone (repo, dir)](#apidoc.element.release-it.git.clone)
- description and source-code
```javascript
function clone(repo, dir) {
  const commitRef = repo.match(commitRefRe),
    branch = commitRef && commitRef[0] ? commitRef[0].replace(/^\#/, '') : 'master';
  repo = repo.replace(commitRef, '');
  return sequence([
    run.bind(null, 'rm', '-rf', dir),
    run.bind(null, 'git', 'clone', repo, '-b', branch, '--single-branch', dir)
  ]);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.release-it.git.commit"></a>[function <span class="apidocSignatureSpan">release-it.git.</span>commit (path, message, version)](#apidoc.element.release-it.git.commit)
- description and source-code
```javascript
function commit(path, message, version) {
  return run(
    'git',
    'commit',
    config.isForce ? '--allow-empty' : '',
    '--message="${util.format(message, version)}"',
    path
  ).catch(err => {
    log.debug(err);
    log.warn('Nothing to commit. The latest commit will be tagged.');
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.release-it.git.getChangelog"></a>[function <span class="apidocSignatureSpan">release-it.git.</span>getChangelog (options)](#apidoc.element.release-it.git.getChangelog)
- description and source-code
```javascript
function getChangelog(options) {
  function runChangelogCommand(command) {
    return run(command).then(result => {
      process.stdout.write('\n');
      config.setRuntimeOption('changelog', result.output);
      return options;
    });
  }

  if(options.changelogCommand) {
    if(options.changelogCommand.match(/\[REV_RANGE\]/)) {
      const previousVersion = config.getRuntimeOption('previousVersion');
      const previousTag = util.format(options.src.tagName, previousVersion);
      return tagExists(previousTag).then(hasTag => {
        const command = options.changelogCommand.replace(/\[REV_RANGE\]/, hasTag ? '${previousTag}...HEAD' : '');
        return runChangelogCommand(command);
      }).catch(err => {
        log.warn('Probably the current version in package.json is not a known tag in the repository.');
        throw new Error('Could not create changelog from latest tag (${previousTag}) to HEAD.');
      });
    } else {
      return runChangelogCommand(options.changelogCommand);
    }
  } else {
    return noop;
  }
}
```
- example usage
```shell
...
  throw new Error('Unable to get remote Git url.')
});
}

function getChangelog() {
const options = config.options;
if(options.github.release) {
  return git.getChangelog(options);
}
}

function checkGithubToken() {
const options = config.options;
if(options.github.release) {
  const token = git.getGithubToken(options.github.tokenRef);
...
```

#### <a name="apidoc.element.release-it.git.getGithubToken"></a>[function <span class="apidocSignatureSpan">release-it.git.</span>getGithubToken (tokenRef)](#apidoc.element.release-it.git.getGithubToken)
- description and source-code
```javascript
function getGithubToken(tokenRef) {
  const token = process.env[tokenRef];
  config.setRuntimeOption('github_token', token);
  return token;
}
```
- example usage
```shell
...
    return git.getChangelog(options);
  }
}

function checkGithubToken() {
  const options = config.options;
  if(options.github.release) {
    const token = git.getGithubToken(options.github.tokenRef);
    if(!token) {
      throw new Error('About to release to GitHub, but ${options.github.tokenRef} environment variable not set');
    }
  }
}

function releaseSourceRepo() {
...
```

#### <a name="apidoc.element.release-it.git.getLatestTag"></a>[function <span class="apidocSignatureSpan">release-it.git.</span>getLatestTag ()](#apidoc.element.release-it.git.getLatestTag)
- description and source-code
```javascript
function getLatestTag() {
  return run('!git', 'describe --tags --abbrev=0').then(result => {
    const latestTag = result && result.output ? result.output.trim() : null;
    return latestTag;
  });
}
```
- example usage
```shell
...
function parseVersion() {

  const options = config.options;
  const version = util.isValidVersion(options.increment) ? options.increment : options.npm.version;

  if(!version) {

return git.getLatestTag().then(tag => {
  if(tag) {
    const nextVersion = util.increment(tag, options.increment, options.prereleaseId);
    log.bold(util.format('Latest tag: %s. Next version: %s', tag, nextVersion));
    config.setRuntimeOption('previousVersion', tag);
    config.setRuntimeOption('version', nextVersion);
  } else {
    throw new Error('Error detecting current version from latest tag.');
...
```

#### <a name="apidoc.element.release-it.git.getRemoteUrl"></a>[function <span class="apidocSignatureSpan">release-it.git.</span>getRemoteUrl ()](#apidoc.element.release-it.git.getRemoteUrl)
- description and source-code
```javascript
function getRemoteUrl() {
  return run('!git', 'config --get remote.origin.url').then(result => {
    if(result && result.output) {
      return result.output.trim();
    }
    throw new Error('Could not get remote Git url.');
  });
}
```
- example usage
```shell
...
  } else {
    config.setRuntimeOption('previousVersion', version);
    config.setRuntimeOption('version', util.increment(version, options.increment, options.prereleaseId));
  }
}

function setRemoteGitUrl() {
  return git.getRemoteUrl().then(remoteUrl => {
    config.setRuntimeOption('remoteUrl', remoteUrl);
  }).catch(err => {
    throw new Error('Unable to get remote Git url.')
  });
}

function getChangelog() {
...
```

#### <a name="apidoc.element.release-it.git.hasChanges"></a>[function <span class="apidocSignatureSpan">release-it.git.</span>hasChanges (repo)](#apidoc.element.release-it.git.hasChanges)
- description and source-code
```javascript
function hasChanges(repo) {
  // Inverted: reject if run promise is resolved (i.e. 'git diff-index' returns exit code 0)
  return when.promise(resolve => {
    run('!git', 'diff-index --name-only HEAD --exit-code').then(() => {
      if(!config.isDryRun) {
        config.setRuntimeOption('${repo}_has_changes', false);
        log.warn('Nothing to commit in ${repo} repo. The latest commit will be tagged.');
      }
      resolve();
    }).catch(resolve);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.release-it.git.isGitRepo"></a>[function <span class="apidocSignatureSpan">release-it.git.</span>isGitRepo ()](#apidoc.element.release-it.git.isGitRepo)
- description and source-code
```javascript
function isGitRepo() {
  return run('!git', 'rev-parse --git-dir');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.release-it.git.isWorkingDirClean"></a>[function <span class="apidocSignatureSpan">release-it.git.</span>isWorkingDirClean (requireCleanWorkingDir)](#apidoc.element.release-it.git.isWorkingDirClean)
- description and source-code
```javascript
function isWorkingDirClean(requireCleanWorkingDir) {
  return requireCleanWorkingDir ? run('!git', 'diff-index --name-only HEAD --exit-code').catch(() => {
    throw new Error('Working dir must be clean.');
  }) : noop;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.release-it.git.push"></a>[function <span class="apidocSignatureSpan">release-it.git.</span>push (remoteUrl, pushUrl)](#apidoc.element.release-it.git.push)
- description and source-code
```javascript
function push(remoteUrl, pushUrl) {
  const repository = pushUrl || '';
  return run('git', 'push', repository).catch(err => {
    log.error('Please make sure an upstream remote repository is configured for the current branch. Example commands:\n' +
      'git remote add origin ${remoteUrl}\n' +
      'git push --set-upstream origin master');
    throw new Error(err);
  });
}
```
- example usage
```shell
...
  repo.stageDir,
  repo.hasChanges
];

if(options.dist.repo) {
  // Before committing to src repo, do some potentially problematic dist repo tasks.
  const distRepoTasks = getDistRepoTasks(options);
  executeTasks.push(distRepoTasks.clone);
  executeTasks.push(distRepoTasks.copy);
  executeTasks.push(distRepoTasks.pushd);
  executeTasks.push(distRepoTasks.bump);
  executeTasks.push(distRepoTasks.beforeStageCommand);
  executeTasks.push(distRepoTasks.stageDir);
  executeTasks.push(distRepoTasks.hasChanges);
  executeTasks.push(distRepoTasks.popd);
...
```

#### <a name="apidoc.element.release-it.git.pushTags"></a>[function <span class="apidocSignatureSpan">release-it.git.</span>pushTags (version, pushUrl)](#apidoc.element.release-it.git.pushTags)
- description and source-code
```javascript
function pushTags(version, pushUrl) {
  const repository = pushUrl || '';
  return run(
    'git',
    'push',
    '--follow-tags',
    config.isForce ? '--force' : '',
    repository
  ).catch(() => {
    log.error('Could not push tag(s). Does tag "${version}" already exist? Use --force to move a tag.');
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.release-it.git.release"></a>[function <span class="apidocSignatureSpan">release-it.git.</span>release (options, remoteUrl, tagName)](#apidoc.element.release-it.git.release)
- description and source-code
```javascript
function release(options, remoteUrl, tagName) {
  const repo = repoPathParse(remoteUrl);
  const version = config.getRuntimeOption('version');

  log.execution('node-github releases#createRelease', repo.repository);

  const githubClient = initGithubClient(repo),
    attempts = 3;
  var success = false;

  if(!config.isDryRun) {
    return when.iterate(
      attempt => attempt + 1,
      attempt => success || attempt === attempts,
      attempt => when.promise(resolve => {
        githubClient.repos.createRelease({
          owner: repo.owner,
          repo: repo.project,
          tag_name: util.format(tagName, version),
          name: util.format(options.github.releaseName, version),
          body: config.getRuntimeOption('changelog'),
          prerelease: options.github.preRelease
        }, (err, response) => {
          if(err) {
            log[attempt + 1 < attempts ? 'warn' : 'error']('${err.defaultMessage} (Attempt ${attempt + 1} of ${attempts})');
            log[attempt + 1 < attempts ? 'warn' : 'error'](err.message);
          } else {
            log.execution('node-github', response.meta.location, response.tag_name, response.name);
            log.verbose(response.body);
            success = true;
          }
          resolve();
        });
      }),
      0
    );
  } else {
    return noop;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.release-it.git.stage"></a>[function <span class="apidocSignatureSpan">release-it.git.</span>stage (file)](#apidoc.element.release-it.git.stage)
- description and source-code
```javascript
function stage(file) {
  if(file) {
    const files = typeof file === 'string' ? file : file.join(' ');
    return run('git', 'add', files).catch(error => {
      log.warn('Could not stage ${file}');
    });
  } else {
    return noop;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.release-it.git.stageDir"></a>[function <span class="apidocSignatureSpan">release-it.git.</span>stageDir (baseDir)](#apidoc.element.release-it.git.stageDir)
- description and source-code
```javascript
function stageDir(baseDir) {
  baseDir = baseDir || '.';
  return run('git', util.format('add %s --all', baseDir));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.release-it.git.status"></a>[function <span class="apidocSignatureSpan">release-it.git.</span>status ()](#apidoc.element.release-it.git.status)
- description and source-code
```javascript
function status() {
  return run(
    '!git',
    'status --short --untracked-files=no'
  ).then(result => {
    // Output also when not verbose
    !config.isVerbose && log.log(result.output);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.release-it.git.tag"></a>[function <span class="apidocSignatureSpan">release-it.git.</span>tag (version, tag, annotation)](#apidoc.element.release-it.git.tag)
- description and source-code
```javascript
function tag(version, tag, annotation) {
  return run(
    'git',
    'tag',
    config.isForce ? '--force' : '',
    '--annotate',
    '--message="${util.format(annotation, version)}"',
    util.format(tag, version)
  ).then(() => {
    config.setRuntimeOption('tag_set', true);
  }).catch(() => {
    log.warn('Could not tag. Does tag "${version}" already exist? Use --force to move a tag.');
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.release-it.shell"></a>[module release-it.shell](#apidoc.module.release-it.shell)

#### <a name="apidoc.element.release-it.shell.build"></a>[function <span class="apidocSignatureSpan">release-it.shell.</span>build (command)](#apidoc.element.release-it.shell.build)
- description and source-code
```javascript
function build(command) {
  return command ? runTemplateCommand(command) : noop.then(() => {
    log.verbose('No build command was provided.');
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.release-it.shell.bump"></a>[function <span class="apidocSignatureSpan">release-it.shell.</span>bump (file, version)](#apidoc.element.release-it.shell.bump)
- description and source-code
```javascript
function bump(file, version) {
  if(file) {
    log.execution('bump', file, version);
  }
  if (!config.isDryRun && file !== false) {
    const files = typeof file === 'string' ? [file] : file;
    return when.map(files, file => fn.call(fs.readFile, path.resolve(file)).then(data => {
      const pkg = JSON.parse(data.toString());
      pkg.version = version;
      return pkg;
    }, err => {
      log.warn('Could not read ${err.path || file}');
      log.debug(err);
    }).then(data => {
      if(data){
        return fn.call(fs.writeFile, file, '${JSON.stringify(data, null, 2)}\n');
      }
    }).catch(err => {
      log.warn('Could not bump version in ${file}');
      log.debug(err);
    }));
  } else {
    return noop;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.release-it.shell.copy"></a>[function <span class="apidocSignatureSpan">release-it.shell.</span>copy (files, options, target)](#apidoc.element.release-it.shell.copy)
- description and source-code
```javascript
function copy(files, options, target) {
  log.execution('copy', files, options, target);
  return !config.isDryRun ? globcp(files, options, target) : noop;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.release-it.shell.mkCleanDir"></a>[function <span class="apidocSignatureSpan">release-it.shell.</span>mkCleanDir (dir)](#apidoc.element.release-it.shell.mkCleanDir)
- description and source-code
```javascript
function mkCleanDir(dir) {
  return sequence([
    run.bind(null, 'rm', '-rf', dir),
    run.bind(null, 'mkdir', '-p', dir)
  ]);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.release-it.shell.npmPublish"></a>[function <span class="apidocSignatureSpan">release-it.shell.</span>npmPublish (path, tag)](#apidoc.element.release-it.shell.npmPublish)
- description and source-code
```javascript
function npmPublish(path, tag) {
  const publishPath = path || '.';
  return run('npm', 'publish', publishPath, '--tag', tag);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.release-it.shell.popd"></a>[function <span class="apidocSignatureSpan">release-it.shell.</span>popd ()](#apidoc.element.release-it.shell.popd)
- description and source-code
```javascript
function popd() {
  return run('popd');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.release-it.shell.pushd"></a>[function <span class="apidocSignatureSpan">release-it.shell.</span>pushd (path)](#apidoc.element.release-it.shell.pushd)
- description and source-code
```javascript
function pushd(path) {
  return run('pushd', path);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.release-it.shell.run"></a>[function <span class="apidocSignatureSpan">release-it.shell.</span>run (command, commandArgs)](#apidoc.element.release-it.shell.run)
- description and source-code
```javascript
function run(command, commandArgs) {

  const shellCommand = getShellCommand(command.replace(forcedCmdRe, '')),
    cmd = [].slice.call(arguments).join(' '),
    normalizedCmd = cmd.replace(forcedCmdRe, ''),
    args = [].slice.call(arguments, 1),
    silentState = shell.config.silent;

  shell.config.silent = !config.isVerbose;

  log.execution(normalizedCmd);

  if (normalizedCmd === cmd && config.isDryRun) {
    return noop;
  }

  return when.promise((resolve, reject) => {

    if(shellCommand === 'exec') {

      shell.exec(normalizedCmd, (code, output) => {
        if (code === 0) {
          resolve({
            code,
            output
          });
        } else {
          reject(output);
        }
      });

    } else if(shellCommand) {

      resolve(shell[shellCommand].apply(shell, args));

    } else {

      resolve(command.apply(null, args));

    }

    shell.config.silent = silentState;

  });

}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.release-it.shell.runTemplateCommand"></a>[function <span class="apidocSignatureSpan">release-it.shell.</span>runTemplateCommand (command)](#apidoc.element.release-it.shell.runTemplateCommand)
- description and source-code
```javascript
function runTemplateCommand(command) {
  return run(util.template(command, config.context));
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.release-it.tasks"></a>[module release-it.tasks](#apidoc.module.release-it.tasks)

#### <a name="apidoc.element.release-it.tasks.run"></a>[function <span class="apidocSignatureSpan">release-it.tasks.</span>run (options)](#apidoc.element.release-it.tasks.run)
- description and source-code
```javascript
run = function (options) {
  return sequence([
    parseVersion,
    setRemoteGitUrl,
    getChangelog,
    checkGithubToken,
    releaseSourceRepo,
    releaseDistRepo
  ], options)
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.release-it.util"></a>[module release-it.util](#apidoc.module.release-it.util)

#### <a name="apidoc.element.release-it.util.format"></a>[function <span class="apidocSignatureSpan">release-it.util.</span>format (template, replacements)](#apidoc.element.release-it.util.format)
- description and source-code
```javascript
function format(template, replacements) {
  if(template.indexOf('%') === -1) {
    return template;
  } else {
    return util.format.apply(null, arguments);
  }
}
```
- example usage
```shell
...
},
changelogCommand: 'githubReleaseBodyCommand'
};

function fixAndWarn(options, deprecatedOption, cat, opt) {
const log = require('./log'); // TODO: Fix circular ref
if(deprecatedOption in options) {
  log.warn(util.format('Deprecation notice: the option %s will be removed soon. Please use %s${opt ? '.' + opt : ''} instead.',
deprecatedOption, cat));
  if(opt) {
    options[cat][opt] = options[deprecatedOption];
  } else {
    options[cat] = options[deprecatedOption];
  }
  delete options[deprecatedOption];
}
...
```

#### <a name="apidoc.element.release-it.util.increment"></a>[function <span class="apidocSignatureSpan">release-it.util.</span>increment (version, increment, identifier)](#apidoc.element.release-it.util.increment)
- description and source-code
```javascript
function increment(version, increment, identifier) {
  increment = increment || 'patch';
  if (releaseTypes.indexOf(increment) === -1) {
    return increment;
  } else {
    return semver.inc(version, increment, identifier);
  }
}
```
- example usage
```shell
...
  const options = config.options;
  const version = util.isValidVersion(options.increment) ? options.increment : options.npm.version;

  if(!version) {

return git.getLatestTag().then(tag => {
  if(tag) {
    const nextVersion = util.increment(tag, options.increment, options.prereleaseId);
    log.bold(util.format('Latest tag: %s. Next version: %s', tag, nextVersion));
    config.setRuntimeOption('previousVersion', tag);
    config.setRuntimeOption('version', nextVersion);
  } else {
    throw new Error('Error detecting current version from latest tag.');
  }
}).catch(err => {
...
```

#### <a name="apidoc.element.release-it.util.isValidVersion"></a>[function <span class="apidocSignatureSpan">release-it.util.</span>isValidVersion (value)](#apidoc.element.release-it.util.isValidVersion)
- description and source-code
```javascript
function isValidVersion(value) {
  return semver.valid(value);
}
```
- example usage
```shell
...
  config = require('./config'),
  sequence = require('when/sequence'),
  noop = when.resolve.bind(when, true);

function parseVersion() {

  const options = config.options;
  const version = util.isValidVersion(options.increment) ? options.increment : options.npm.version;

  if(!version) {

return git.getLatestTag().then(tag => {
  if(tag) {
    const nextVersion = util.increment(tag, options.increment, options.prereleaseId);
    log.bold(util.format('Latest tag: %s. Next version: %s', tag, nextVersion));
...
```

#### <a name="apidoc.element.release-it.util.template"></a>[function <span class="apidocSignatureSpan">release-it.util.</span>template (input, context)](#apidoc.element.release-it.util.template)
- description and source-code
```javascript
function template(input, context) {
  return _.template(input)(context);
}
```
- example usage
```shell
...
    shell.config.silent = silentState;

  });

}

function runTemplateCommand(command) {
  return run(util.template(command, config.context));
}

function getShellCommand(command) {
  return command && command in shell && typeof shell[command] === 'function' ? command : 'exec';
}

function pushd(path) {
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
