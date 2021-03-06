# Falcon

Falcon is a library which allows you to use the [Cosmos](https://github.com/OpenGenus/cosmos) library in a convenient way. Currently it has features like Search, Recommendation, etc

This repository is based out in python scripts and is currently ported to python 3.x, Now lets begin with the features.

## Installation
Install pipenv and add it to path:  
```bash
pip3 install --user pipenv
```

then install the dependencies from the root of project:  
```bash
pipenv shell
pipenv install
```

##### Clone the Repository
To start first we need to clone the cosmos repository using the ```index.py``` file by writing ```python3 index.py``` command.

##### Search For Files

A simple search for files in the cosmos repo can be done using the command ``` python3 search.py --search="greedy algorithms" --results=3 ``` here we have two options 
- **search(Required)** : We enter the search term here.
- **results(Optional)** : The integer value shows the top number of results, like above shows top 3 results and not specifying any values for it will result in showing ALL results for search.

##### Recommendations

User can seek recommendation for search terms using the command ```python3 recommendations.py --recommend artificial --type parent --top 3``` , here we have two options
- **recommend(Required)** : We enter the recommendation term here.
- **type(Optional)** : By default this value is all which will search for the term in complete directory tree, if parent is entered then only parent directories are recommended and if child is entered then only child directories can be recommended.
- **top(Optional)** : Missing the parameters results in showing of all results and we can enter integers to restrict the number of returned results.

##### Edit/Delete Code
The file ```code.py``` can be used to search the code in a given language in the complete cosmos directory and can be used to edit/ delete code, can be used using the command ``` python3 code.py --term linear --language cpp ``` , this will open the top file matching with term linear in cpp
- **term(Required)** : We enter the search term here.
- **language(Required)** : We enter the language in which we want the final results, the value of the parameter is the extension of language in which code is required.

### Generate List of Implemented Algorithms
#### What's the stats script?
The stats script deals with generating a progress list of the cosmos repo, by taking into account all algorithms currently existing in the repo and categorizing them based on the languages used to implement them.

#### How to run?
**make sure that you're in the falcon project root directory**

#### for generating the output in txt file :-
```bash
python3 stats.py -f txt > ./STATS.txt
```

#### for generating the output in md file :-
```bash
python3 stats.py -f md > ./STATS.md
```

This library is under development, please feel free to report any issues or request a features.
