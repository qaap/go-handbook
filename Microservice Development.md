# Microservice Development

*A work-in-progress article*

When starting to develop backend applications, there are certain things we should pay attention to:
* Golang versions
* Boilerplate reuse
* 3rd party libraries
* Test-Driven Development

## Starting from scratch

We currently use on the latest version of Golang when developing. A same version is also considered for production uses.

## General purpose tools

The tools we use when developing a microservice, and those are mainly python and shell scripts,
are meant to be fetched from our [contrib](https://github.com/elpheria/contrib) project.  
Once the application is *kickstarted*, we could add those tools via git submodule with the following command:

```git submodule add https://github.com/qaap/contrib tools```

You can then add the `tools` directory to your project with `git add tools .gitmodules`.

If there's a need for you to update a submodule while developing your microservice,
make sure you do the following:
* cd into the ```tools``` directory
* checkout to master
* add and commit those changes there
* go back to root directory
* commit a Subproject change there and do a push to contrib like this:

```git push --recurse-submodules=on-demand```

We can also sync a submodule with

```git submodule update --remote --rebase```
