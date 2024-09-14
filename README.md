# hugo-vs-code-container-dev

This repository can be forked to create a hugo development environment in a VS Code Development container.

The documentation here is how to fork and use this repo, not how to create sites in hugo. If you need answers to that then use the hugo documentation.

## Workflow

1. fork repository
2. Setup your site from VS Code Terminal
3. Update your devcontainer.json to start hugo server
4. Start using as you would for normal site dev
5. Configure dev to prod pipelines in the repo (different for each site)

## one-time setup of hugo site

### new site setup (vs code terminal)

In VS Code open a new terminal.

**ctrl-shift-`** or Terminal -> new terminal

#### verify hugo installation

```bash
hugo version
```

Should return a version of hugo installed.

#### create a new hugo site

```bash
hugo new site myhugosite
```

Should create a new hugo site. This site will not include a theme but it will have hugo.toml and other files.

Not that themes can be added a git submodules.

Terminal helpful includes other instructions and a link to the hugo documentation.

#### configuring the container to start hugo on startup

After you successfully have created your site.

You can configure the devcontianer.json to auto start and run the server so you can see your updates as you make them.

In devcontainer.json uncomment the postStartCommand.

```json
	// Use 'postStartCommand' to run commands after the container is started, will run each time.
	// this is commented out until you run the commands in terminal to create your site.
	   "postStartCommand": "hugo version && hugo server -D",
```

### devcontainer.json

This container spins up an ubuntu instance that can be used to create a new hugo site and includes hugo, go, github cli, and git large file system in addition to normal vs code container settings.

It also includes default extensions for VS Code of spell checking, amazon Q, aws settings, and md linter.
