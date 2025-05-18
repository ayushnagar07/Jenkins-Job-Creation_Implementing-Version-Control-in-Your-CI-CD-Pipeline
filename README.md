1. Creating the Jenkins Job
Opened Jenkins and clicked on “New Item”. Created a Freestyle project and named it Newitem. Under the Source Code Management section, selected Git. Entered my GitHub repository URL: https://github.com/ayushnagar07/Jenkins-Job-Creation_Implementing-Version-Control-in-Your-CI-CD-Pipeline Changed the branch specification from master to main, since my GitHub repo uses main as the default branch.

2. Adding Build Steps
In the Build section, I added a Windows batch command. I used the following command to simulate a simple build: echo "Building the project..." This command was added in the “Execute Windows batch command” section and used to verify that Jenkins executes the build step after cloning the repository.

3. Running the Build and Output
Clicked Build Now to trigger the build manually. Viewed the logs under Console Output, which showed the following:
![WhatsApp Image 2025-05-18 at 7 55 19 PM](https://github.com/user-attachments/assets/20cec648-547b-4ee7-92ff-2ff9b12453c1)

This confirmed that Jenkins successfully: Fetched the code from GitHub Checked out the correct commit Executed the batch command Finished the build successfully

4. Challenges Faced and Solution
I initially got an error: “Couldn't find any revision to build.” This happened because Jenkins was looking for the master branch, which didn’t exist in my GitHub repo. I resolved it by changing the branch specifier in Jenkins to main.
![WhatsApp Image 2025-05-18 at 7 55 19 PM (1)](https://github.com/user-attachments/assets/e8c2cf8e-72b6-41fb-a055-7a88f4b7ce8b)
