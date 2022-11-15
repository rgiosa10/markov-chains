# Markov Chains

#### By Ruben Giosa

#### This repo includes an exercise for my solution to a Markov Chain that uses a sonnet as input data, organize the data by the frequency with which one word follows any other, and then provide a predictive recommended word (using the sonnet) based a user inputted word from the sonnet.

<br>

## Technologies Used

* Python
* Git
* Markdown
* Jupyter Notebooks
* `.gitignore`
* `requirements.txt`

</br>

## Description

A Markov chain is one kind of predictive model that guesses the next event based on the current event. Markov chains are used by cell phones, for instance, to guess which word you're going to type into a text next. Here's how it works: each time a word is encountered, the Markov chain keeps a tally of how often different words follow it. For example, let's say you sent the following four texts:
- "good morning"
- "good gracious"
- "good morning"
- "good job"

We see that the word 'good' was followed by 'morning' twice, by 'gracious' once, and by 'job' once. How can we organize this information for use in a Markov chain? One way is with nested dictionaries, like this:
```python
{current_word1: {following_word1: num_of_times, following_word2: num_of_times, following_word3: num_of_times}}
```
...in our example, it would look like:
```python
{'good': {'morning': 2, 'gracious': 1, 'job':1}}
```
What if we then sent another text, reading "good morning, sunshine"? Now we have 'good' followed by 'morning' another time, and 'morning' followed by 'sunshine' once. So now our nested dictionary looks like this:
```python
{'good': {'morning': 3, 'gracious': 1, 'job':1}, 'morning':{'sunshine': 1}}
```
To summarize:
- The outer dictionary contains each word from the input text as a key, followed by an inner dictionary as a value
- Each inner dictionary contains as keys the words that can follow each key in the outer dictionary, with the number of times they actually follow that word as the value

In this challenge, it takes some Shakespeare sonnets as input data, organizes the data by the frequency with which one word follows any other, and then provide a predictive recommended word (using the sonnet) based a user inputted word from the sonnet.

<br>

## Setup/Installation Requirements

* Go to https://github.com/rgiosa10/markov-chains.git to find the specific repository for this website.
* Then open your terminal. I recommend going to your Desktop directory:
    ```bash
    cd Desktop
    ```
* Then clone the repository by inputting: 
  ```bash
  git clone https://github.com/rgiosa10/markov-chains.git
  ```
* Go to the new directory or open the directory folder on your desktop:
  ```bash
  cd python-intermed-1-cr
  ```
* Once in the directory you will need to set up a virtual environment in your terminal:
  ```bash
  python3.7 -m venv venv
  ```
* Then activate the environment:
  ```bash
  source venv/bin/activate
  ```
* Install the necessary items with requirements.txt:
  ```bash
    pip install -r requirements.txt
  ```
* With your virtual environment now enabled with proper requirements, open the directory:
  ```bash
  code .
  ```

</br>

## Known Bugs

* No known bugs

<br>

## License

MIT License

Copyright (c) 2022 Ruben Giosa

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

</br>