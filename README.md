# google-apps-script-dts

Generates @types/google-apps-script.

```sh

```

## Create a PR to DefinitelyTyped

1. Fork https://github.com/DefinitelyTyped/DefinitelyTyped
1. Run the following script, but rename `grant` to your GitHub username.

```sh
# Clone repos in a new directory.
git clone git@github.com:grant/google-apps-script-dts.git
git clone git@github.com:DefinitelyTyped/DefinitelyTyped.git

# Delete old types
rm -rf DefinitelyTyped/types/google-apps-script/

# Generate types
cd google-apps-script-dts;
npm run build;
npm run generate;
cd ..;
cp google-apps-script-dts/types/google-apps-script/ DefinitelyTyped/types/google-apps-script/
cd DefinitelyTyped;

# View Changes
git diff

# Update GitHub
git add -A
git commit -m '[types/google-apps-script] Generate Types ($(date +%Y-%m-%d)'
git push
```

Then open on GitHub and create a PR to DefinitelyTyped.

## GitHub Template

Fill out the GitHub PR with the following details:

Title: `[types/google-apps-script] Generate Types`

Body:
```
- [x] Use a meaningful title for the pull request. Include the name of the package modified.
- [x] Test the change in your own code. (Compile and run.)
- [x] Add or edit tests to reflect the change. (Run with `npm test`.)
- [x] Follow the advice from the [readme](https://github.com/DefinitelyTyped/DefinitelyTyped/blob/master/README.md#make-a-pull-request).
- [x] Avoid [common mistakes](https://github.com/DefinitelyTyped/DefinitelyTyped/blob/master/README.md#common-mistakes).
- [x] Run `npm run lint package-name` (or `tsc` if no `tslint.json` is present).

Select one of these and delete the others:

If changing an existing definition:
- [x] Provide a URL to documentation or source code which provides context for the suggested changes: https://developers.google.com/apps-script/reference/
- [x] Increase the version number in the header if appropriate.
- [x] If you are making substantial changes, consider adding a `tslint.json` containing `{ "extends": "dtslint/dt.json" }`.
```

## Previous Work

Also see:
https://github.com/motemen/dts-google-apps-script