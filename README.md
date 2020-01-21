
# cs400-S2020-lab01-starter

Designed for use with [GitHub Classroom](https://classroom.github.com/), this repository contains the starter files for the lab of this course.

## Summary

In this lab, you will be three writing programs in C. The objectives are the following.
* Part1: A introduction program in C. The program must compile correctly and must complete the following tasks.

  * Ask the user for a first name
  * Ask the user for a last name
  * Ask the user for a first random number.
  * Ask the user for a second random number.
  * Print a greeting using the first and last name.
  * Print the favorite numbers and their sum.

* Part 2: Choose two (2) basic system calls.
  * Explain why they are described as _system calls_ and then write a small program in C (for each) to demonstrate how each system call works using a library.
  * For example, such a system call may be used to check for the existence of a file. In your work, please make sure this task is clear to the reader to be able to understand the code.
  * If your code or explanation is inspired from a source other than your class textbook, please be sure to offer a complete citation of the source (i.e., website, article, book, etc.).

## Testing your programs
This assignment uses [Docker](https://www.docker.com) to compile and run C programs without installing C compiler locally.
First, you need to make sure you have installed [Docker
Desktop](https://www.docker.com/products/docker-desktop) and have it running.
Next, you need to build the Docker container by running the following command in the terminal:
`docker build -t gccdev .`
Then, you can run the Docker container using the following command:
`docker run -it gccdev`
Now, you can mount the local drive and run the container :
`docker run -it --mount type=bind,source=$PWD,target=/home/gccdev gccdev`
Finally, you can use `gcc filename.c -o filename` to run your C program named `filename`

## Using GatorGrader to verify the submission
For this assignment you can use you can use the [GatorGrader
tool](https://github.com/GatorEducator/gatorgrader) run in another Docker container
to verify that the minimal content of your programs and a reflection document satisfies the
requirements specified in the lab assignment sheet. Once you have finished the
implementation of all programs and before you make your final submission,
run the GatorGrader application to start `gradle grade` as a containerized
application, using the [DockaGator](https://github.com/GatorEducator/dockagator)
Docker image available on
[DockerHub](https://cloud.docker.com/u/gatoreducator/repository/docker/gatoreducator/dockagator).
First, to ensure that the following command will work correctly, you
must create the cache directory by running the command `mkdir
$HOME/.dockagator`.
Then, to see if your submission satisfies the minimal requirements, you can run the following command in the terminal:

```bash
docker run --rm --name dockagator \
  -v "$(pwd)":/project \
  -v "$HOME/.dockagator":/root/.local/share \
  gatoreducator/dockagator
```

This command will use `"$(pwd)"` (i.e., the current directory) as
the project directory and `"$HOME/.dockagator"` as the cached GatorGrader
directory. Please note that both of these directories must exist, although only
the project directory must contain something. Generally, the project directory
should contain the source code and technical writing of this assignment, as
provided to a student through GitHub. Additionally, the cache directory should
not contain anything other than directories and programs created by DockaGator,
thus ensuring that they are not otherwise overwritten during the completion of
the assignment.  If the above `docker run` command does not work correctly on
the Windows operating system, you may need to instead run the following command
to work around limitations in the terminal window:

```bash
docker run --rm --name dockagator \
  -v "$(pwd):/project" \
  -v "$HOME/.dockagator:/root/.local/share" \
  gatoreducator/dockagator
```

## Assistance

If you are having trouble completing any part of this project, then please talk with either the course instructor or a tech-leader during the lab session. You can also schedule a meeting during the course instructor's office hours.
