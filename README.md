# hello-git-tagging

## Variables

```console
export GIT_NEW_VERSION=0.0.0
export GIT_NEW_VERSION_MSG="Updated version"
```

## Adding a new tag

`git` commands to tag the current state of the master branch in the local repository
and push the changes to the "origin" (example origin: GitHub.com).

```console
git checkout master
git pull
git tag \
  --annotate \
  --message "${GIT_NEW_VERSION_MSG}" \
  ${GIT_NEW_VERSION}
git push origin ${GIT_NEW_VERSION}
```

## Deleting a tag

`git` commands to delete a tag in the local repository
and push the changes to the "origin" (example origin: GitHub.com).

```console
git checkout master
git tag --delete ${GIT_NEW_VERSION}
git push origin :refs/tags/${GIT_NEW_VERSION}
```

## References

1. [Git Basics - Tagging](https://git-scm.com/book/en/v2/Git-Basics-Tagging)