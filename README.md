# Dependency Caching

When we are running multiple jobs, some steps of these jobs might be duplicated. But when considering the time that takes to execute these steps, installing dependencies takes the most time.

Each new job runs in a new runner. So, dependencies will downloaded to these runners each time a new job executes. So, if we can cache these dependencies and reduce the duration we can save a lot of time from the overall workflow execution.

We can cache the dependencies when they are downloaded in one job and use them in other jobs. We can also use those cashed dependencies in other workflows as well. (Only if the files and folders doesn't change between workflows)

Github actions has a official action to caching files and folders across jobs and workflows.
