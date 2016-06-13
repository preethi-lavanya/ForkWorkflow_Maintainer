1. In this mode, each develper works on his own remote repository.
2. The centralized repository in this case is maintained by the code mainter.
3. Developers who want to work on this repository forks this repository. This can be done from the github UI.
4. The develpers then clone their own remote repository using: git clone <repository URL>
5. They then add as remote upstream the maintainers repository: git add remote upstream <maintainers git url>
6. They add and commit to the local repository.
7. Pull latest changes from public repository using: git pull upstream master
8. They then push to their local remote using: git push.
9. The developer then creates a pull request in the maintainers repository and specifies the url of the branch.
10. The maintainer can then fetch the code into his local code and merge to remote master using:
	git fetch <Developer git URL>;
	git checkout master;
	git merge FETCH_HEAD;
