## Exercise 11.1 - [Warming up](https://fullstackopen.com/en/part11/introduction_to_ci_cd#exercise-11-1)

**Some common steps in a CI setup include linting, testing, and building. What
are the specific tools for taking care of these steps in the ecosystem of the
language you picked?**

### Linting Python

Linting highlights syntactical and stylistic problems in your Python source
code. For Python specifically, the most popular tools for linting are
[Flake8](https://flake8.pycqa.org/en/latest/index.html), and
[Pylint](https://pylint.pycqa.org/en/latest/).

### Testing Python

For testing python here are the most popular modules.
[Unittest](https://docs.python.org/3/library/unittest.html) is a
batteries-included test module in the Python standard library.
[Pytest](https://docs.pytest.org) is a no-boilerplate alternative to Python’s
standard unittest module.

### Building

Python is an interpreted language, so its _"build"_ mainly revolves around test
execution rather than compilation. Nonetheless, you can _"compile"_ a Python
program into an executable with a bundling tool, such as:
[pyexe](http://www.py2exe.org/) or
[cx_freeze](https://cx-freeze.readthedocs.io/en/latest/). To _"compile"_ a
specific _\*.py_ file, you can use
[py_compile](https://docs.python.org/3/library/py_compile.html) or use
[compileall](https://docs.python.org/3/library/compileall.html) to _"compile"_
all modules in a project.

**What alternatives are there to set up the CI besides Jenkins and GitHub
Actions?**

[Travis CI](https://travis-ci.org/) is the oldest and most mature cloud-hosted
CI/CD provider. Travis CI provides support for many languages like Node, PHP,
Python, Java, Perl, and so on. Travis CI can be configured easily by creating a
_.travis.yml_ file in your repository. You can find steps to set up Travis CI
with GitHub
[here](https://docs.travis-ci.com/user/tutorial/#to-get-started-with-travis-ci-using-github).

[CircleCI](https://circleci.com/) is one of the most popular cloud-hosted CI/CD
providers. Circle CI provides support for many build configurations and
languages like Node, Android, Java, Go, Python, Ruby, amongst other languages.
Circle CI can be configured by creating a _.circleci/config.yml_ file in your
repository. You can find steps to set up Circle CI with GitHub/BitBucket
[here](https://circleci.com/docs/2.0/gh-bb-integration/).

**Would this setup be better in a self-hosted or a cloud-based environment? Why?
What information would you need to make that decision?**

For a Python setup, a cloud-based environment would be better, since it doesn't
have any special requirements. However, knowing the scope and size of the
project could change that decision because if it were a larger or more complex
project a self-hosted environment could prove cheaper in the long run.
Furthermore, if there are other projects within the organization that could also
take advantage of the self-hosted environment, then the self-hosted solution
would be even a better choice.
