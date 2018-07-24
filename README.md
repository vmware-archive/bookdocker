
## About Bookdocker

Bookbinder on Docker (bookdocker) is a tool to make a Docker container to run Bookbinder in any Bookbinder book repository.

Bookdocker does the following:

1. Checks if Docker is installed
1. Checks that you are in a `book` directory
1. Creates a custom container with the following:
  1. Ruby v2.3.0
  1. Your book's dependencies, including Bookbinder
1. Runs Bookbinder in the docker container

## How to Install

1. Clone this repo.
   ```
   git clone https://github.com/pivotal-cf-experimental/bookdocker.git
   ```

1. Copy the `bookdocker` file into your executable path. For example:
   ```
   cp ~/workspace/bookdocker /usr/local/bin
   ```

## How to Run

Once you installed bookdocker, do the following:

1. Go to your book directory.

1. Run bookdocker. Bookdocker takes the same commands and arguments that Bookbinder takes.
   ```
   bookdocker watch MY-REPO
   ```

## Known Issues

### Bookdocker is Slower Than Bookbinder on Mac

On large books, bookdocker is slow and may become unusable. To mitigate this issue, watch a single repo at a time. For example, run `bookdocker watch my-content-repo`.

## License

bookdocker is licensed under the MIT license.  See the LICENSE file for more information.
