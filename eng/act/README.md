A Dockerfile for testing with [Act](https://nektosact.com/).

1. Build this file:

    ```sh
    cd eng/act
    docker build . -t local-act-with-pwsh
    ```

2. Run the following, where `$($REPO_ROOT)` is the path to this project:

    ```sh
    act -P ubuntu-latest=local-act-with-pwsh --local-repository darkpatternsdigital/actions@main=$($REPO_ROOT) --pull=false
    ```

    Note that `darkpatternsdigital/actions@main` should match the repo and version, not the additional path.

For more options with Act, run `act --help`.
