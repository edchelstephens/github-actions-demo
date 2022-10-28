# Environment variables and secrets

```

steps:
    - name: Hello World

```

## 2 Ways to pass a secret in workflow
1. As an input using:

```
steps:
    - name: Hello World
        with:
            super_secret_input: ${{ secrets.MySecret }}
```

2. As an environment variable using:
```
steps:
    - name: Hello World
        env:
            super_secret_input: ${{ secrets.MySecret }}
```

# Core Concepts

# Actions
- reusable units of  code
- can use action from marketplace or create your own
- to use an action in a workflow run, you must include it as a step
- these actions are the individual tasks that you combine as steps to create a job in your wokflow file.

# Events
- Specific activites that trigger a workflow run
- using the key: `on:`
- Provide a single event, an array of events or an array of event activity types

# Job
- a job consists of one or more steps
- A step is a set of tasks that can be executed by a job
- Each step of the job executes the same runner, which allows for information sharing like environment variables
- Steps can run commands or actions
- using the keyword `jobs:`
- jobs can run independently or sequentially


# Workflow file
- An automated process that is made up of one or multiple jobs and can be triggered by an event
- Defined using a YAML file in the `.github/workflows` directory

# Runners
- This tells the workflow run where the virtual environment will be
- These are any machines that Github Actions Runner application is installed
- Waits for an available job to be kicked off when an event is triggered
- Only run one jub at a time

# Workflow Run
- This is the instance of your workflow that runs when the pre-configured event occurs.
- You can see the jobs, actions, logs and statuses of each workflow run in the actions log on GitHub's Actions page
# Artifacts
- files created when you build and test your code
- binary, package or log files

# Continuous Integration and Continuous Deployment (CI/CD)
- Create custom Continuous Integration(CI) to automate building and testing of your code
- Create custom Continuous Deployment(CD) to automatically deploy your code to any cloud, self-hosted service, or platform from your repository





