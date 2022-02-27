![](https://i.imgur.com/iywjz8s.png)


# Day 4 Collaborative Document

2022-02-14 How to write good code: CodeRefinery

Welcome to The Workshop Collaborative Document.

This Document is synchronized as you type, so that everyone viewing this page sees the same text. This allows you to collaborate seamlessly on documents.

----------------------------------------------------------------------------

## 👮Code of Conduct

* Participants are expected to follow those guidelines:
* Use welcoming and inclusive language.
* Be respectful of different viewpoints and experiences.
* Gracefully accept constructive criticism.
* Focus on what is best for the community.
* Show courtesy and respect towards other community members.

## ⚖️ License

All content is publicly available under the Creative Commons Attribution License: [creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/).

## 🙋Getting help

To ask a question, type `/hand` in the chat window.

To get help, type `/help` in the chat window.

You can ask questions in the document or chat window and helpers will try to help you.

## 🖥 Workshop website

[link](https://esciencecenter-digital-skills.github.io/2022-02-14-ds-cr/)

🛠 Setup

[link]([<url>](https://esciencecenter-digital-skills.github.io/2022-02-14-ds-cr/#Setup))

## 👩‍🏫👩‍💻🎓 Instructors

Sven, Hanno, Leon

## 🧑‍🙋 Helpers
Aron, Robin, Jaro

## 👩‍💻👩‍💼👨‍🔬🧑‍🔬🧑‍🚀🧙‍♂️🔧 Roll Call
Name/ pronouns (optional) / job, role / social media (twitter, github, ...) / background or interests (optional) / city

## 🗓️ Agenda
| | |
|-|-|
|9:00| Welcome and icebreaker|
|9:15| Testing with pytest|
|10:15| Coffee break|
|10:30| Testing with pytest|
|11:45|Coffee break|
|12:00| Continuous Integration|
|12:45| Wrap-up|
|13:00| END|

## 🧊 Icebreaker
Which is a nice book that you read recently?
- SuperIntelligence Nick Bostrom
- What the dog saw. Malcolm Gladwell
- The Catcher in the Rye by J. D. Salinger :+1::+1:
- Homo Deus by Yuval Noah Harari
- Rules of Civilty by Amor Towles
- The Witcher including prequels by Andrzej Sapkowski (:+1::+1:)
- Jade City and sequels by Fonda Lee
- Physics for Future Presidents - Richard A. Muller
- De meeste mensen deugen (humankind: a hopeful history) by Rutger Bregman
- Debt: The First 5000 Years by David Graeber :+1::+1:
- The dawn of everything (David Graeber and David Wengrow)
- Spike by Jeremy Farrar
- The Tipping Point by Malcolm Gladwell
- Basta Marco van Basten
- On earth we are briefly gorgeous by Ocean Wong
- The unconsoled - Kazuo Ishiguro
- I only read books on flights or long travels ..., and since covid I haven't had the chance. (tv series or movies are also fine!) Casa de papel:+1:
## 🔧 Exercises

## 🧠 Collaborative Notes
### Testing
*"Controlling complexity is the essence of computer programming"* Brian Kernighan
All the tools that we teach are about controlling complexity.
Also testing is about this.

Tests help preserving expected functionality:
* As projects grow, it becomes easier to break things without noticing immediately
* Software defects can be caused by both human errors and non-controllable events
* Testing helps detecting new errors early
* Interpreted dynamically typed imperative languages often need to be tested
* So do complied languages but the compiler catches at least some errors
* Testing is essential for research software because we care about reproducibility
* Program testing can be used to show the presence of bugs, but never show their abscence!

Tests help users of your code:
* Make it easier for others to verify the code has been correctly installed
* Provide basis to judge the quality of the code
* USers of your code publish papers based on results produced by your code
* Your peers need to be able to reproduce your published computational results

Tests help other developers:
* Tests make it easier to refactor the code (rewrite coe while keeping functionality)
* Code can become unsustainable without ruunable tests
* Documenation which is up to date by definition
* Easier for external developers to contribute without breaking the code

**So testing is important for yourself, collaborators, and users**

How to test?
* Test frequently
* Test automatically
* Tesst with numerical tolerance
* Think about code coverage (which fraction of your code is tested?)

Defensive programming
* Assume that mistakes will happen and introduce guards against them.
* Use assertions for things you believe should never happen
* Use exceptions for anomalous or exceptional conditions requiring special processing

Types of test:
* Unit test: really test one function
* Integration test: How do modules or program as a whole work together
* Regression test: Test a specific core feature, so to be sure that they still work if the rest of the code is adapted

Tests from a larger perspective
* Code coverage matters (which fraction of your code is tested?)
* Tests don't guarantee correctness
* There are multiple testing frameworks
* Continuous integration (automated tests in Github) are important

[Sonarcloud](https://sonarcloud.io/)
* Linked to a github repository
* Framework that inspects your code and can find:
    -  bugs
    -  security hotspots
    -  code smells (code is correct, but the way you wrote it is bad)

### Hanno's test demo
`example.py`:
```python=
def add(a, b):
    return a + b

def test_add():
    assert add(2, 3) == 5
    assert add('space', 'ship') == 'spaceship'
    assert add(0.1, 0.2) == 0.3
```

You need to install pytest, run:
```
pip install pytest
```

Run tests by calling:
```
pytest -v example.py
```

### Unit testing exercise: Four functions to write tests for
Start by discussing how you would design tests for the following four functions, and then try to write the tests. Below are the Python versions of the code, but you can also work on the C++, R, Julia or Fortran versions of the code. They can be supplied by one of the helpers.
#### 1
```python=
def factorial(n):
    """
    Computes the factorial of n.
    """
    if n < 0:
        raise ValueError('received negative input')
    result = 1
    for i in range(1, n + 1):
        result *= i
    return result
```
#### 2
```python=
def count_word_occurrence_in_string(text, word):
    """
    Counts how often word appears in text.
    Example: if text is "one two one two three four"
             and word is "one", then this function returns 2
    """
    words = text.split()
    return words.count(word)
```
#### 3
```python=
def count_word_occurrence_in_file(file_name, word):
    """
    Counts how often word appears in file file_name.
    Example: if file contains "one two one two three four"
             and word is "one", then this function returns 2
    """
    count = 0
    with open(file_name, 'r') as f:
        for line in f:
            words = line.split()
            count += words.count(word)
    return count
```
#### 4
```python=
class Pet:
    def __init__(self, name):
        self.name = name
        self.hunger = 0
    def go_for_a_walk(self):  # <-- how would you test this function?
        self.hunger += 1
```

#### Solutions:

##### Room 2 Lannie, Luisa, Ediz, Pavlo
```python
#1
def test_factorial():
    assert factorial(6) == 720
    with pytest.raises(ValueError, match='received negative input'):
        factorial(-2)
```
``` python
#2
def test_count_word_occurrence_in_string():
    assert count_word_occurrence_in_string("Counts how often word appears in text.", "often") == 1
    assert count_word_occurrence_in_string("aa aaa aa aaaa aa aaa aaaa aaa aaaa", "aa") == 3
    assert count_word_occurrence_in_string("", "x") == 0
    assert count_word_occurrence_in_string("one", "") == 0
    assert count_word_occurrence_in_string("     ", " ") == 0

```
``` python
#3
def test_count_word_occurrence_in_file():
    assert count_word_occurrence_in_file('test_file.txt','one') == 2
    assert count_word_occurrence_in_file('test_file.txt','four') == 1
    assert count_word_occurrence_in_file('test_file.txt','dog') == 0
    assert count_word_occurrence_in_file('test_emptyfile.txt','dog') == 0
```
##### Room 3 Ecem, Meixin, Diana, Aron
```python
def test_factorial():
    assert factorial(3) == 6
    assert factorial(0) == 1
    assert factorial(1) == 1
    with pytest.raises(ValueError):
        factorial(-1)

def test_count_word_occurrence_in_string():
    assert count_word_occurrence_in_string("one two one two three four", "one") == 2
    assert count_word_occurrence_in_string("one two one two three four", "two") == 2
    assert count_word_occurrence_in_string("one two one two three four", "five") == 0
    assert count_word_occurrence_in_string("", "one") == 0
    assert count_word_occurrence_in_string("", "") == 0

def test_count_word_occurrence_in_file():
    with open('readme.txt', 'w') as f:
        f.write("one two one two three four")

    assert count_word_occurrence_in_file("readme.txt", "one") == 2

    os.remove("readme.txt")

def test_go_for_a_walk():
    dog = Pet("Oslo")
    assert dog.hunger == 0
    dog.go_for_a_walk()
    assert dog.hunger == 1
    dog.go_for_a_walk()
    assert dog.hunger == 2
```

##### Room 4
```python=
def test_factorial():
    assert factorial(1) == 1
    assert factorial(0) == 1
    assert factorial(3) == 6
    with pytest.raises(ValueError):
        factorial(-1)
    with pytest.raises(TypeError):
        factorial('hello')
        factorial(1.2)

def test_count_word_occurrence_in_string():
    assert count_word_occurrence_in_string("one two one two three four", "one") == 2
    assert count_word_occurrence_in_string("some text", "two") == 0
    assert count_word_occurrence_in_string('AAAAA', 'AAA') == 0
    assert count_word_occurrence_in_string("hello 'how' are you", "how") == 0
    with pytest.raises(AttributeError):
        assert count_word_occurrence_in_string(123, "word") == 0


def test_Pet():
    dog = Pet("peter")
    assert dog.name == "peter"
    assert dog.hunger == 0
    dog.go_for_a_walk()
    assert dog.hunger == 1
```
##### Room 5
```python=
def test_Room5_factorial():
    assert factorial(1) == 1
    assert factorial(4) == 24
    with pytest.raises(ValueError) as exc_info:
        factorial(-1)
    assert """received negative input""" in str(excinfo.value)

    ## less obvious behaviour
    assert factorial(0) == 1
    with pytest.raises(TypeError) as exc_info:
        factorial(3.5)
    assert """TypeError: 'float' object cannot be interpreted as an integer""" in str(excinfo.value)
```
```python=
def test_room5_count_word_occurrence_in_string():
    test_func = count_word_occurrence_in_string
    assert test_func("one two one two three four", "one") == 2
    assert test_func("one two one two three four", "five") == 0
    assert test_func("one two one two three four", "") == 0
    assert test_func("", "") == 0
    assert test_func("", "nothing") == 0
    assert test_func(b"one two one two three four", b"one") == 2
    assert test_func(b"one two one two three four", b"five") == 0
    assert test_func(b"one two one two three four", b"") == 0
    ## when mixing types
    assert test_func(b"one two one two three four", "one") == 0
    assert test_func(b"one two one two three four", "five") == 0
    assert test_func(b"one two one two three four", "") == 0
```

##### Room 6
###### 1
```python=
from pytest import raises
def test_factorial():
    with raises(Exception):
        factorial(-1)
    with raises(Exception):
        factorial(0.1)
    assert factorial(3) == 6
    assert factorial(10) == 3628800
    assert factorial(20) == 2432902008176640000
    assert factorial(5) == 5*4*3*2*1
    assert factorial(5) == 120
```
###### 2
```python=
def test_count_word_occurrence_in_file():
    assert count_word_occurrence_in_file('test.txt', 'hello') == 6
    assert count_word_occurrence_in_file('test.txt', 'hi') == 0
    # actually we believe the test is correct but the function itself is incorrect
    # the function doesn't force a str type input parameter
    # but doesn't work for any other input
    assert count_word_occurrence_in_file('test.txt', 5) == 0
    assert count_word_occurrence_in_file('test.txt', 6) == 1
```
###### 3
```python=
def test_count_word_occurence_in_string():
    assert count_word_occurrence_in_string("Hello world", "world") == 1
    assert count_word_occurrence_in_string("Hello world", "wworld") == 0
    assert count_word_occurrence_in_string("Hello world Hello world Hello world Hello world", "world") == 4
```
###### 4


#### Room 1: Chiara, Daniel, Friederike, Khaleel
```python=
import pytest

def test_factorial():
    assert factorial(0) == 1
    assert factorial(1) == 1
    assert factorial(2) == 2
    assert factorial(6) == 720
    assert factorial(8) != 40000
    with pytest.raises(ValueError):
        assert factorial(-1)
    with pytest.raises(TypeError):
        assert factorial("test")

def test_count_word_occurrences():
    assert count_word_occurrence_in_string("one two one", "one") == 2
    assert count_word_occurrence_in_string("one two one", "four") == 0
    assert count_word_occurrence_in_string("one two one", "o") == 0
    assert count_word_occurrence_in_string("one, two, three", "one") == 0 # technically it should be 1

def test_count_word_occurrence_in_file():
    assert count_word_occurrence_in_file("test.txt", "one") == 2
    assert count_word_occurrence_in_file("test.txt", "four") == 0
    assert count_word_occurrence_in_file("test.txt", "o") == 0
    with pytest.raises(FileNotFoundError):
        assert count_word_occurrence_in_file("wrong.txt", "one")

def test_Pet():
    dog = Pet("cat")
    assert dog.name == "cat"
    assert dog.name != "dog"
    assert dog.hunger == 0
    dog.go_for_a_walk()
    assert dog.hunger == 1
```
### Continuous integration
I won't add notes for this part, because we will do the exact same thing as Hanno's demonstration in the exercise.

### Exercise: Full-cycle collaborative workflow
This is an expanded version of the automated testing demonstration. The exercise is performed in a collaborative circle within the exercise group (breakout room).

The exercise takes 30-40 minutes.

In this exercise, everybody will:

A. Create a repository on GitHub/GitLab (everybody should use a different repository name for their repository)
B. Commit code to the repository and set up tests with GitHub Actions/ GitLab CI
C. Everybody will find a bug in their repository and open an issue in their repository
D. Then each one will clone the repo of one of their exercise partners, fix the bug, and open a pull request (GitHub)/ merge request (GitLab)
E. Everybody then merges their co-worker’s change

![](https://i.imgur.com/UR6Qaue.png)
Overview of this exercise. Below we detail the steps.

#### Step 1: Create a new repository on GitHub/GitLab

- Select a different repository name than your colleagues (otherwise forking the same name will be strange)
- Before you create the repository, select “Initialize this repository with a README” (otherwise you try to clone an empty repo).
- Share the repository URL with your exercise group via shared document or chat

#### Step 2: Clone your own repository, add code, commit, and push

Clone the repository.

Add a file `example.py` containing:

```python=
def add(a, b):
    return a + b


def test_add():
    assert add(2, 3) == 5
    assert add('space', 'ship') == 'spaceship'


def subtract(a, b):
    return a + b  # <--- fix this in step 8


# uncomment the following test in step 5
#def test_subtract():
#    assert subtract(2, 3) == -1

```
Test `example.py` with `pytest`.

Then stage the file (`git add <filename>`), commit (`git commit -m "some commit message"`),
and push the changes (`git push origin main`).


#### Step 3: Enable automated testing

In this step we will enable GitHub Actions.
- Select "Actions" from your GitHub repository page. You get to a page "Get started with GitHub Actions".
- Select the button for "Set up this workflow" under Python Application.

![](https://i.imgur.com/7QOplAg.png)
Select “Python application” as the starter workflow.

GitHub creates the following file for you in the subfolder `.github/workflows`:


   ```yaml
# This workflow will install Python dependencies, run tests and lint with a single version of Python
# For more information see: https://help.github.com/actions/language-and-framework-guides/using-python-with-github-actions

name: Python application

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  build:

    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v2
    - name: Set up Python 3.9
      uses: actions/setup-python@v2
      with:
        python-version: 3.9
    - name: Install dependencies
      run: |
        python -m pip install --upgrade pip
        pip install flake8 pytest
        if [ -f requirements.txt ]; then pip install -r requirements.txt; fi
    - name: Lint with flake8
      run: |
        # stop the build if there are Python syntax errors or undefined names
        flake8 . --count --select=E9,F63,F7,F82 --show-source --statistics
        # exit-zero treats all errors as warnings. The GitHub editor is 127 chars wide
        flake8 . --count --exit-zero --max-complexity=10 --max-line-length=127 --statistics
    - name: Test with pytest
      run: |
        pytest
   ```

Replace `pytest` by `pytest example.py`:
```yaml
   - name: Test with pytest
     run: |
       pytest example.py
```
![](https://i.imgur.com/1TFZPRe.png)


Commit the change by pressing the "Start Commit" button.

#### Step 4: Verify that tests have been automatically run

Observe in the repository how the test succeeds. While the test is executing, the repository has a yellow marker.
This is replaced with a green check mark, once the test succeeds.

![](https://i.imgur.com/b8dI8XH.png)

Green check means passed.

Also browse the "Actions" tab and look at the steps there and their output.

#### Step 5: Add a test which reveals a problem

After you committed the workflow file, your GitHub/GitLab repository will be ahead of your local cloned repository. Update your local cloned repository:

```
$ git pull origin main
```
or
```
$ git pull origin master
```
Next uncomment the code in `example.py` under “step 5”, commit, and push. Verify that the test suite now fails on the “Actions” tab (GitHub) or the “CI/CD->Pipelines” tab (GitLab).


#### Step 6: Open and issue on GitHub/GitLab
Open a new issue in your repository about the broken test (click the “Issues” button on GitHub or GitLab and write a title for the issue). The plan is that your colleague will fix the issue through a pull/merge request

#### Step 7: Fork and clone the repository of your colleague

Fork the repository using the GitHub/GitLab web interface.

Make sure you clone the fork after you have forked it. Do not clone your colleague’s repository directly.

```
$ $ git clone https://gitlab.com/your-username/the-repository.git
```

#### Step 8: Fix the broken test

After you have fixed the code, commit the following commit message `"restore function subtract; fixes #1"` (assuming that you try to fix issue number 1).

Then push to your fork.

#### Step 9: Open a pull request (GitHub)/ merge request (GitLab)

Then before accepting the pull request/ merge request from your colleague, observe how GitHub Actions/ Gitlab CI automatically tested the code.

If you forgot to reference the issue number in the commit message, you can still add it to the pull request/ merge request: `my pull/merge request title, closes #NUMBEROFTHEISSUE`

#### Step 10

Observe how accepting the pull request/ merge request automatically closes the issue (provided the commit message or the pull request/ merge request contained the correct issue number).

Discuss whether this is a useful feature. And if it is, why do you think is it useful?

### Recap
Think about what you learned in this course (git, collaboration with Github, modular code, documentation, testing, continuous integration)
* What questions do you still have?
* Whether there are any incremental improvements that can benefit your projects?
* What’s nice that we learnt but is overkill for your current work?

- Ajey
- Arista
- Ayda
- Chiara
    - Ok, you convinced me to try and reorganize my code, but do you have any suggestions/resources on how to set up for example a python project from scratch (e.g. how to organize files structurally, how to (eventually) use environments, basically where to start from)? --> I think I found something on the NLeSC github page:
        - a very complete guide on almost everything we discussed in the course and more: https://guide.esciencecenter.nl/#/
        - a python project template: https://github.com/NLeSC/python-template
- Daniel
    - no questions; using modular code; also using modular code :slightly_smiling_face:
- Diana
- Duco
    - No questions
    - Rewriting plotting and analysis functions to be seperate. adding snakemake to my workflow from the beginning
    - Testing might be a bit overkill at this stage but will be great in the future
- Ecem
- Ediz
- Esther
    - No questions
    - How to make more use of issues via Gihub, and I have gained more confidence that I already know a lot about efficiently developing and maintaining research software
    - Testing via Gihub, due to the large amount of input data
- Khaleel
- Krist
- Lannie
    - Plenty but that's what we have stackoverflow for;
    - Will definitely try Sphinx, SonarCloud and CI, really nice to learn new tools
    - None of this seems like overkill (I guess if you don't implement tests you will regret it later and have to do it anyway, at least for bigger projects)
- Luisa
- Masa
    - Q1: none; Q2: documentation, modular code, (maybe testing); Q3: continuous integration,documentation webpages (e.g. sphinx)
- Meixin
- Yanick
- Sjors
    - Questions about separting files and importing/packages/modules/etc.
    - I'm sure I will use everything I learned
    - Probably nothing is overkill (except forking maybe)

### feedback for today:
#### Top (what went well):
* CI is really awesome & like the full cycle assignment a lot! (:+1:)
*
* Really liked the last exercise, explanations were very well written (:+1::+1::+1:)
#### Tip (what can be improved):
* Teach something about separting files (e.g. for code separation and separate test files)
* In general, exercises can be made a bit more complex / difficult. While coding itself is not the main focus, having more realistic (and thus more difficult) examples do help in understanding (:+1:)
* Today at the start was a bit less interactive at the start than other days, maybe a bit more hands-on or code-along could change that
## 📚 Resources
Please fill in the [post-workshop survey](https://www.surveymonkey.com/r/JZWD92B)
[Pytest `assert` documentation (including how to check for expected exceptions)](https://docs.pytest.org/en/latest/assert.html)

[Example github workflow with matrix testing](https://github.com/NLeSC/python-template/blob/main/%7B%7Bcookiecutter.directory_name%7D%7D/.github/workflows/build.yml)
[NLeSC Python cookiecutter template](https://github.com/NLeSC/python-template)
[pre-commit hooks](https://git-scm.com/book/en/v2/Customizing-Git-Git-Hooks) (If you want to setup automated tests before you commit your code)
