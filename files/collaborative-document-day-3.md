![](https://i.imgur.com/iywjz8s.png)


# Day 3 Collaborative Document

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
|9:15| Modular code|
|10:15| Coffee break|
|10:30| Modular code|
|11:45| Coffee break|
|12:00| Documentation|
|12:45| Wrap-up|
|13:00| END|

## 🧊 Icebreaker
What is your most brilliant failure?

 - Daniel: Building a PC, installing the CPU cooler upside-down
 - Hanno: Had rsync delete all my files through a cron job after 13 months into my Ph.D. after one of the hard drives had been replaced. That cron job was meant for backup.
 - Aron: leaving a bold-face todo comment in a published paper
 - Ajey: The experiments in one of my papers were wrong and I had to retract it after it got accepted.
 - Duco: Made a critical calculation mistake in my masters due to using really bad analysis pipelines and bad versioning.
 - Duco: pushed a private key to github and forgot to remove it from other branches :')
 - Kobus: After months of salsa class, I did a first zouk class last Friday. This caused me to forget all the salsa moves yesterday at salsa class
 - Lannie: Forgot to pick my daughter up from school not once but twice in about 4 months time. Also lost 2Gb of data by mistyping a password somewhere.
 - Sven: Deleting the production elasticsearch index (sort of the backend of a search engine) on the last day of the year, which broke the search functionality of my previous company
 - Masa: A recent one was trying to debug some code for four days, only to find out that I capitalised the name of a method which should have been lower case
 - Kat: I'm a mediocre powerlifter (but still much stronger than when I started)
 - Luisa: first bike ride in Liège, thought 100 km easy! I didnt realized that there were >1000 m ascension and after 75 km I was dead, my phone was dead, rookie mistake: underestimating the belgian mountains.
- Robin: Maxed out inodes on supercomputer and brought it down for several days/months during phd
- Kristi: Parking in a flea market place, found my car sourrounded by very mad flea market sellers.
- Khaleel: One day I've decided to try tennis and used my badminton skills (wrist movements rather than shoulder movements). Due to the heavier racket, I injured my wrist badly.
- Leon: Accidentally rebooted a remote server instead of the local PC I was using
- Meixin: Removing a chat app without backup the chatting records. Therefore losing many good memories.
- Ediz: After a show, forgot my pedalboard at the middle of the main street. After less than 30 minutes, I had to go over the police bridge to take my pedals from the bomb squad. They were almost exploding it...
- Chiara: tripping on the microphone cable on stage while make the winner pitch during an hackaton competition where I was describing how we could help patients with mobility problems with our app.
- Jaro: Hit someone actually in the face while trying to explain some movie scene where someone was hit in the face.
- Friederike: accidentally publishing my password to the whole university
- Yanick: I accidentally ran a command (qkill) to kill all jobs of the current user instead of ending all submitted jobs (scancel?) as root on a remote server instead of running as a local user. IT had to go over to physically restart the server.





## 🧠 Collaborative Notes

### Exercise: Think of good and bad examples
Write down your thoughts in the collaborative documents.
Respond with emojis :+1: :scream_cat: to your colleagues' answers.

- Think of projects of which you like the documentation. What do you like about them?
    - Rust documentation -> very clear and conciseust documentation
    - shapely: Very good explanations for what each function does in their library. Wherever necessary, the documentation also explains a little bit of the math so that an average user can understand.
    - maybe a bit generic, but git actually has some really clear and well structured documentation on their commands :+1::+1:
    - Pyradiomics: Has a really nice website where you can find everything you need. They also have a search function
    - DESeq2: Lots of examples that use real data, clear explanation of WHY a given choice is made
    - Linux file-systems from 80's. Everyting is apart and well documented even in alien languages.
    - tar: tab gives you all the options and their explanations!
    -
    - Cisco Prime API. Good naming convention and clear documentation on colums
    -
- Think of projects for which you don’t like the documentation. What don’t you like about them? Are you missing anything?
    - Biopython-> they just do not explain or even list all of the options for a lot of the functions -> you need to actually dig into the code sometimes
    - Nextflow -> very sparse documentation, does not mention many vital functions, nor optional arguments.
    - PowerFactory -> very elaborate documentation, spread out over numerous files often needing more than one to solve a problem and still some problems not solveable
    - PIL: Too many documentation websites for different versions. It's too much hassle.
    - Snakemake -> It's 200 million pages long and still doesn't explain itself well.
    - SPM (fMRI toolbox for data analysis): the code is not entirely open, documentation is not really explanatory (input/output, meaning of parameters). Correct usage comes with experience or by asking somebody with experience.
    - Paraview

    - A colleague's code to design a new MRI sequence in already existing code: the biggest problem for me was that naming and comments where not-consistent (and sometimes just not existing) plus lot's of hard-coded not-explained stuff
    - Most of the Jupyter projects. Everything gets outdated within hours, the most of the code has documentation from previous versions.
    - Building systems API's Most of them don't explain there columns
**NB: You can choose a mature library with lots of users for this exercise, but try to also think of less mature projects you had to collaborate on, or papers you had to reproduce.**






### Exercise: Writing good comments
Let's take a look at two example comments (comments in python start with `#`):
#### Comment A
```python=
# Now we check if temperature is larger then -50:
if temperature > -50:
    print('do something')
```

#### Comment B
```python
# We regard temperatures below -50 degrees as measurement errors
if temperature > -50:
    print('do something')
```
 Which of these comments is best? Can you explain why?
 Write your answer in the collaborative document (before looking at others' answers)


#### Answers
| Name | Answer |
|------|--------|
Ajey |The second comment makes more sense as we already know what the line of code is doing. But we need to know why we want to do it when we read code.
Ayda |The second one because it explains why we want to check whether is below -50 or not.
Chiara | The second, since the first one is kind of already obvious and doesn't explain why that lines are added, what is their intended functionality
Daniel | A only explains one of the two lines. B explains the concept of the two lines
Diana | The second comment. THe first one is too obvious - can be easily seen from the code. The
Duco | B is best because the check is obvious from the code.
Ecem | B, we already know what the if statement does
Ediz | Neither. A doesn't have a proper argument, B doesn't actually raise an error
Esther |
Friederike | The second one: it tell you the why, the first comment is just kind of pseudocode of the actual code
Kat | B Tells you "why" instead of just "what", which is self-explanatory
Khaleel | B, more specific explanation especially when you're working on a specific project
Kobus | A, because B makes the assumption that "do something" regards -50 as measurement errors. A is less specific
Lannie | Second, the first just repeats the code, the second explains the reason for the code
LIANYU |
Lolke | The code only does something with temperature above -50, so I prefer A although not explicit.
Luisa | B. A is redundant, B gives you extra info.
Masa |B is better because it explains why we check for specific temperatures (A just puts `>` in words)
Meixin | A. The command line isn't show below -50 directing error.
Pavlo | The second one, because it tells why tells why tells why tells why tells why tells why tells why tells why tells why tells why
Sjors | Comment
Yanick |
Yiyun | B. B explained more about the purpose of these lines.
Kristi | B. explains the purpose of the statement.


### Docstrings

```python=
import pandas
```

```python=
def mean_temperature(data):
    temperatures = data['Air temperature (degC)']
    return sum(rtempratures)/len(temperatures)
```

Let's add a docstring
```python=
def mean_temperature(data):
    """
    Get the main temperature

    Args:
        data (pandas.DataFrame): A pandas dataframe with
            air temperature measurements. The column
            'Air temperature (degC)' should be in there.
    Returns:
        The mean air temperature (float)
    """
    temperatures = data['Air temperature (degC)']
    return sum(rtempratures)/len(temperatures)
```

To see the documentation for your function, use python's `help()` function:
```python=
help(mean_temperature)
```



### Exercise: Adding in-code documentation

 Update this code snippet so it is well-documented:

 ```python
 import pandas as pd

 def x(a, print_columns=False):
    b = pd.read_excel(a)
    column_headers = list(b.columns.values)
    if print_columns:
        print("\n".join(column_headers))
    return column_headers
 ```
 1. One person screen-shares, discuss and together converge on a final solution. (8 minutes)
 2. Share final solution in collaborative document.

#### Answers
##### Breakout room 1 (Diana, Esther, Meixin)
```python=
import pandas as pd

def get_headers(file_name, print_columns=False):
    '''
    Reads excel file and returns column headers
    :param file_name: is the name of the file, string
    :param print_columns: prints the column headers, optional, boolean
    :return: the column headers, list
    '''
    data = pd.read_excel(file_name)
    column_headers = list(data.columns.values)
    if print_columns:
        print("\n".join(column_headers))
    return column_headers
```

##### Breakout room 2 (Duco, Lannie, Lolke)
```python
import pandas as pd


def read_excel_column_headers(filename, print_columns=False):
    """
    Reads column headers from excel file and optionally prints them.
    :param filename: name of the excel file
    :param print_columns: boolean, default False
    :return: list of column headers
    """
    df = pd.read_excel(filename)
    column_headers = list(df.columns.values)
    if print_columns:
        print("\n".join(column_headers))
    return column_headers
```

##### Breakout room 3 (Chiara, Ediz, Kat)
```python=
'''
Optionally prints column headers from excel file

Arguments:
	a: path to input excel file [string]
	print_columns: boolean to toggle column names printing in output [bool]

Return:
	column_headers: list of strings of column headers [list]
'''
```

##### Breakout room 4 (Ayda, Kobus, Masa)
```python
import pandas as pd

def x(a, print_columns=False):
	"""
	Extract column headers from excel file

	Args:
		a (Excel file): An excel file with at least one column
		with column names
		print_columns (boolean): Optional print of column headers

	Returns:
		Column headers (list of strings). Can be printed as well.
	"""
   # Read the excel file into a pandas data frame
   b = pd.read_excel(a)
   # Extract the column headers
   column_headers = list(b.columns.values)
   # Optionally, print the column headers to console
   if print_columns:
       print("\n".join(column_headers))
   return column_headers
```

##### Breakout room 5 (Ajey, Sjors, Yanick)

```python
import pandas as pd

def get_excel_headers(path_to_file: str, print_columns:bool = False) -> list:
    """
    Get the headers from an excel file.

    Parameters
    ----------
    path_to_file: str
        A string that gives path to the excel file.
    print_columns: bool
        A boolean flag to determine if you want to print the column headers during runtime.

    Return
    ------
    column_headers: list
        A list of headers
    """
   df = pd.read_excel(path_to_file)
   column_headers = list(df.columns.values)
   if print_columns:
       print("\n".join(column_headers))
   return column_headers
```




##### Breakout room 6 (Daniel, Khaleel)

```python=
 import pandas as pd

 def return_column_headers(data_sheet, print_columns=False):
 """
    Reads the data of an excel sheet and returns the names of each column.
    Optionally prints all names in the console in new lines.

    Args:
        data_sheet : Excel sheet data
        print_columns: (optional) should names be printed in the console
    Returns:
        returns the names of each column as a list
 """
    b = pd.read_excel(data_sheet)
    column_headers = list(b.columns.values)
    if print_columns:
        print("\n".join(column_headers))
    return column_headers
```

##### Breakout room 7 (Friederike, Krist, Liyiyun)

 ```python
import pandas as pd

def read_columns(dataFile, print_columns=False):
    """
    Reads and prints the column headers

    Args: dataFile, the directory of the targeted file
          print_columns, if True it will print the column headers

    Returns: the column headers in a list
    """

    dataFrame = pd.read_excel(dataFile)
    column_headers = list(dataFrame.columns.values)
    if print_columns:
         print("\n".join(column_headers))
    return column_headers
 ```
##### Breakout room 8 (Luisa, Pavlo, Aron)
```python
import pandas as pd

def get_column_headers(file_name:str, print_columns:bool =False ) -> list:
   """
      Function that returns a list with the colum headers of the excel file.
      Optionally prints the column headers
      Args:
         file_name: path of the excel file containing the data
         print_columns (optional): boolean, if True, column headers are printed.
      Returns: list containing the headers of the columns
   """
   data = pd.read_excel(file_name)
   column_headers = list(data.columns.values)
   if print_columns:
       print("\n".join(column_headers))
   return column_headers
   ```






 ### Exercise: Write a README file
 You are going to write a README file for an example project.

 #### The example project
 Here's [the example project](https://github.com/escience-academy/coderefinery-documentation-example-project).
 For this project we transformed the code snippets from the previous episode into a single script [analyse_spreadsheet.py](https://github.com/escience-academy/coderefinery-documentation-example-project/blob/main/analyse_spreadsheet.py)

 Let's take a look at [the script](https://github.com/escience-academy/coderefinery-documentation-example-project/blob/main/analyse_spreadsheet.py).
 You don't need to understand the script completely, all you need to know is:
 * The functions `mean_temperature` and `get_spreadsheet_columns` from previous episode are in there.
 * We added a `main` function that is called when you run the script
 (you could run this python script by calling `python analyse_spreadsheet.py` on the command line).
 It will prompt the user for a file name, print the columns in the spreadsheet, and print the mean
 temperature.

 That's all there is to this project! (You can ignore the other files in the repository, we'll get back to them in episode 4)

 #### The exercise (20 minutes)
 1. One person shares the screen and is the driver. The others are 'navigators' and tell the 'driver' what to do.
 1. Fork [the example project](https://github.com/escience-academy/coderefinery-documentation-example-project) to your own github namespace
 2. Add a file called `README.md` (you can use the github web interface or work locally (i.e. `git clone`, edit the file,  `git add`, `git commit`, `git push`))
 3. Add some content to your README file. Think about what you want the audience to know about your project!
    It does not matter whether the information is correct, it is more important that you have all the components that make up a good README file.
 4. Note that the README file is nicely rendered on the github repository page.

 NB: The `README.md` file is written in 'Markdown' a very popular lightweight markup language, all you need to know for now is this syntax:
 ```
 # A section title
 ## A subsection title
 Normal text

 A list with items
 - item1
 - item2
 ```

 (Optional): Use [https://hemingwayapp.com/](https://hemingwayapp.com/) to analyse your README file and make your writing bold and clear!

**Post a link to your README in the answers below!**

#### Answers
| Room | Link |
|------|------|


### Recap modular coding, documentation + collaborative Git + Github
* What questions do you still have?
* Whether there are any incremental improvements that can benefit your projects?
* What’s nice that we learnt but is overkill for your current work?



### Feedback
### Tops
- Learned a lot of handy tricks such as click, docstrings and sphinx (:+1: :+1: :+1:)
- Things I've learned today I'll be able to use in current and future projects
- Explanation on DocStrings was very good
- Great tips on important aspects of programming
- Great to learn how to use DocStrings properly
- Seeing Leon code and giving suggestions :+1:
### Tips
- a bit more time for the hands-on part (seconded)
- combine the first part with what we learned about Git in previous days
- It would have been nice to have some hands-on practice with Sphinx
- Some of the tools were a bit Python-specific, would be nice to see alternatives for other languages
- I would encourage use of verbosity argumens to the program. The you can differentiate in when writing warnings/errors
- Fully / further integrating use of git and GH with examples and excersises would really drive home git usage. Maybe we can work on the same git repo during the whole week.

## 📚 Resources
[git cheatsheet](https://about.gitlab.com/images/press/git-cheat-sheet.pdf)

Follow the coderefinery material from here to create sphnix/readthedocs documentation: https://coderefinery.github.io/documentation/sphinx/

Checkout [Sphinx autodoc documentation](https://www.sphinx-doc.org/en/master/usage/quickstart.html#autodoc) for autogenerating documenation based on docstrings.

For anyone going through the material above and having an issue with the prerequisites, you need to install sphinx_rtd_theme separately, apparently it used to be a dependency of sphinx but not anymore. You can also ignore it, you just won't be able to use this theme later.
