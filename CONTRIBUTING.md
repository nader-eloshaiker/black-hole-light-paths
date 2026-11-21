# Contributing

Thanks for your interest in improving Black Hole Light Paths.

## Reporting a problem

Open an [issue](https://github.com/nader-eloshaiker/black-hole-light-paths/issues/new/choose) and include:

- what you expected and what happened
- your browser, its version, and your operating system
- a screenshot if the picture looks wrong

## Physics corrections

If something in the simulation or the explanations is physically wrong, please open an issue with a short explanation and, where possible, a reference.

## Making changes

1. Fork the repository and create a branch from `main`.
2. Edit `index.html`. It is self-contained: the styles, the WebGL shader and the side-view code are all in that one file.
3. Open the file in a browser and check the picture at 0°, around 8° and at 90°, with gravity at 0% and 100%.
4. Open a pull request describing what changed and why.

Keep the page dependency-free and working without a build step.

## Code of conduct

This project follows the [Code of Conduct](CODE_OF_CONDUCT.md).
