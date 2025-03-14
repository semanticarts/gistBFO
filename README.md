# gistBFO
A BFO compatible version of Gist

## Setting Up the Local Repository
- Clone this repository
- Run the script `./tools/setup.cmd`. This script will work on Windows, Linux, and Mac. It copies the `./tools/pre-commit` hook into `.git/hooks`, which means it will run before every commit you make to the repository.

The pre-commit hook does several things when you run `git commit`:

- Prevents commits to the branches `develop` and `main`.
- Runs the serializer. This converts files into a standard Turtle format in order to remove noise in the diffs. As the comments in the file indicate, you should use the pre-approved version of `rdf-toolkit.jar` in this directory, rather than another version that you may have elsewhere on your local drive.
- Note: Any PR containing unserialized commits will be returned for correction.
