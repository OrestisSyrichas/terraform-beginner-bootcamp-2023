# _Terraform Beginner Bootcamp 2023_

#### Symantic Versioning :mage:
This project is going to utilize the symantec versiong for tagging
[https://semver.org/](https://semver.org/)

The general format is **MAJOR.MINOR.PATCH** e.g. `1.0.1`

- **MAJOR** version when you make incompatible API changes
- **MINOR** version when you add functionality in a backward compatible manner
- **PATCH** version when you make backward compatible bug fixes
Additional labels for pre-release and build metadata are available as extensions to the **MAJOR.MINOR.PATCH** format.


##### Working Env Vars

### env command

We can list all our environment variables using the `env` command 

We can filter specific env vars using `grep` command e.g. `env|grep aws`

#### Setting and unsetting env vars
In the terminal we can set using  `export HELLO='WORLD'`
In the terminal we can unset using `unset HELLO`

We can set an env var temporarily when just running a command 

```sh
HELLO= 'world' ./bin/print_message

```
Within a bash script we can set an env var without writing export eg.

```
HELLO=`world`

echo $HELLO

```
#### Printing env vars

We can print an env var using echo eg. `echo $HELLO`

###### Scoping of Env Vars

When you open up a new bash terminal in VSCODE it will not be aware of env vars that you have set in another window.

If you want Env Vars to persist across all feature bash terminals that are open you need to set Env Vars in your bash profile. eg. `bash_profile`


###### Persisting Env Vars in GitPod 

We can persist env vars in gitpod by storing them in Gitpod Secret Storage.

```````
gp env HELLO=`world`

```````

All future workspace vars will set the env vars for all bash terminals opened in those workspaces.
You can also set env vars in `.gitpod.yml` but this can only contain non-sensitive env vars.


### AWS CLI Installation

AWS CLI is installed for this project via the bash script `./bin/Install_AWS_CLI.sh` [`./bin/Instal_AWS_CLI.sh`](./bin/Install_AWS_CLI.sh)
 

[Getting Started Install (AWS CLI)](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)

We can check if our AWS credentials is configured correctly by running the following command:

```sh
aws sts get-caller-identity
```

