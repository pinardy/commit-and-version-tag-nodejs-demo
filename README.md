# commit-and-version-tag demo

### Commands

To try out what happens with a new release, run the following command:

```
npm run release-patch -- --dry-run
```

To create a new patch release, run the following command:

```
npm run release-patch
```

Different flags can be added for different release types (major/minor/patch). Refer to `package.json` for the various flags

Upon running the release command, the tool will do the following:

1. Create a commit that updates the following files:

- `package.json`
- `package-lock.json`
- `CHANGELOG.md`

2. Create a new git tag

You will have to push this commit in yourself. If you have run the command incorrectly, you can undo the commit and manually delete the git tag by running `git tag` to check the list of git tags and then delete the specific tag with `git tag -d v1.1.0`.
