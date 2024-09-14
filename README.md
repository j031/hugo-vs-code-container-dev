# hugo-vs-code-container-dev

This repository can be forked to create a hugo development environment in a VS Code Development container.

## Workflow

1. fork repository
2. Setup your site
3. 

### configuring you hugo site first time
You will need to run the hugo commands to create new a new site and load your theme. 

After that go to the devcontianer.json and setup hugo to auto start and run the server so you can see your updates as you make them.

```json
	// Use 'postStartCommand' to run commands after the container is started, will run each time.
	// this is commented out until you run the commands in terminal to create your site.
	   "postStartCommand": "hugo version && hugo server -D",
```

### devcontainer.json

This container spins up an ubuntu instance that can be used to create a new hugo site.

After you ini

