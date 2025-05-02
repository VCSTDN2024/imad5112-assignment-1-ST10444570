Utilisation of GitHub and GitHub Actions
1. name: This is the name of the workflow that appears on GitHub when the action is run.

2. env: These are environment variables accessible to all jobs and steps in the workflow. In this case, main_project_module is set to app, and playstore_name is set to IIECat.

3. on: This section defines the events that will trigger the workflow. In this case, the workflow will run when thereâ€™s a push to the release branch or when the workflow is manually triggered from the Actions tab (workflow_dispatch).

4. jobs: This section contains all the jobs that will be run in the workflow. In this case, thereâ€™s only one job named build.

5. runs-on: This specifies the type of machine to run the job on. Here, itâ€™s set to run on the latest version of Ubuntu.

6. steps: These are the individual tasks that make up a job. 
   Each step can run commands (run:), run setup tasks (uses:), or 
   set job-level environment variables. 	
   The steps include checking out the repository; 
	- setting up Java, 
	- running tests, 
	- building the project, 
	- creating APKs and AABs, and 
	- uploading the build artifacts to GitHub.

7. uses: This is used to include external actions. For example, actions/checkout@v3 checks out your repository onto the runner, and actions/setup-java@v3 sets up a JDK environment for use in actions.

8. with: This is used to specify inputs for the uses: steps.

9. run: This is used to run command-line programs using the operating systemâ€™s shell.
