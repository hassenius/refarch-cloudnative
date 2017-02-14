## Contributing to the BlueCompute Reference Application
Anyone can contribute to the BlueCompoute Reference Application and associated projects and we welcome your contributions.
There are multiple ways to contribute: report bugs and improvement suggestion, improve documentation and contribute code.

We really value contributions and to maximize the impact of code contributions we request that any contributions follow these guidelines:

## Coding Standard 
- Please ensure you follow the coding standard and code formatting used throughout the existing code base
- All files must have the MIT license header included
- All new features must be accompanied by associated tests

## Creating pull requests
- Make sure all tests pass locally before submitting a pull request
- New pull requests should be created against the integration branch of the repository.   
  This ensures new code is included in full stack integration tests before being merged into the master branch.


## House keeping

1. One feature / bug fix / documentation update per pull request
2. Include tests with every feature enhancement, improve tests with every bug fix
3. One commit per pull request (squash your commits)
4. Always pull the latest changes from upstream and rebase before creating pull request. 


### Github and git flow
The internet is littered with guides and information on how to use and understand git.
However, here's a compact guide that follows the suggested workflow

1. Fork the desired repo in github

        
2. Clone your repo to your local computer


3. Add the upstream repository

    Note: Guide for step 1-3 here: [forking a repo](https://help.github.com/articles/fork-a-repo/](https://help.github.com/articles/fork-a-repo/)

4. Create new development branch off the integration branch

    ```
    git checkout -b <my-feature-dev> integration
    ```
5. Do your work
   - write your code
   - write your tests
   - pass your tests locally
   - commit your intermediate changes as you go and as appropriate
   - repeat until satisfied

6. Rebase to the latest upstream changes, resolving any conflicts

    ```
    git fetch upstream
    git branch --set-upstream-to=upstream/integration
    git rebase
    ```

7. Create a new branch off the integration branch to submit pull request from
    
    ```
    git checkout -b <my-feature> integration
    ```

8. Squash your intermediate commits development branch into a single commmit in feature branch

    ```
    git merge --squash <my-feature-dev>
    git commit -m 'add feature xyz'
    ```


9. Push the changes to your repository

    ```
    git push origin <my-feature>
    ```

10. Create pull request

[Creating a pull request](https://help.github.com/articles/creating-a-pull-request/)

Remember: Create the pull request from your feature branch to our `integration` branch

