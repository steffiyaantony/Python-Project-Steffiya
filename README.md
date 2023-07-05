# Python-Project-Steffiya

The code written here is a Python script that allows users to select a genre, year, and rating to retrieve a random movie recommendation from IMDb. 
Below is the breakdown of how the code works with the concepts learnt in training like ****Pandas programs**, Error handling, conditional loops, web scraping**:
1.	The script imports necessary libraries: requests for making HTTP requests, BeautifulSoup for parsing HTML, and pandas for data manipulation.
2.	It uses web scraping with the help of the requests and BeautifulSoup libraries to fetch movie data from IMDb's website.
3.	It defines a list of movie genres (genere_list) and a function (randomizer) to select a random item from a list.
4.	The script enters a while loop to prompt the user to select a genre from the available genre list or quit the program. If the user enters a valid genre, the loop breaks. If the user enters "quit," the program terminates. Otherwise, it asks for correct input.
5.	It constructs the URL based on the selected genre and sends an HTTP GET request to IMDb's website using requests.get.
6.	The HTML content of the response is parsed using BeautifulSoup to extract relevant movie data.
7.	A pandas DataFrame (movie_df) is created to store the movie information.
8.	The script iterates over each movie in the parsed HTML and extracts the movie name, year, PG rating, runtime, and rating. It handles any potential exceptions that may occur during extraction.
9.	The extracted movie information is added to the movie_df DataFrame using append.
10.	Another while loop is entered to prompt the user to select a year from the available years in the movie_df DataFrame or choose "any" for a random movie. If the user enters a valid year, the loop breaks. If the user chooses "any," the loop breaks and includes all movies. Otherwise, it asks for correct input.
11.	A third while loop is entered to prompt the user to select a rating or choose "any" for a random movie. If the user enters a valid rating, the loop breaks. If the user chooses "any," the loop breaks and includes all movies. Otherwise, it asks for correct input.
12.	The script filters the movie_df DataFrame based on the selected year and rating.
13.	Finally, a random movie name is selected from the filtered DataFrame using the randomizer function, and it is printed as a recommendation.
