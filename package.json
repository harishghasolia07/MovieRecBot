import random

# Dummy movie data
movies = [
    {
        "title": "The Shawshank Redemption",
        "genre": ["Drama"],
        "director": "Frank Darabont",
        "cast": ["Tim Robbins", "Morgan Freeman"],
        "release_year": 1994,
        "rating": 9.3
    },
    {
        "title": "The Godfather",
        "genre": ["Crime", "Drama"],
        "director": "Francis Ford Coppola",
        "cast": ["Marlon Brando", "Al Pacino"],
        "release_year": 1972,
        "rating": 9.2
    },
    # Add more movie data...
]

def recommend_movies(user_preferences):
    recommended_movies = []
    for movie in movies:
        if all(genre in movie["genre"] for genre in user_preferences["genre"]):
            if user_preferences["director"] in movie["director"]:
                if any(actor in movie["cast"] for actor in user_preferences["actors"]):
                    if movie["release_year"] >= user_preferences["release_year"]:
                        recommended_movies.append(movie)
    return recommended_movies

def chat():
    print("Welcome to the Movie Recommendation Chat Bot!")
    print("Please provide your movie preferences.")

    user_preferences = {
        "genre": input("Genre(s) you prefer (comma-separated): ").split(","),
        "director": input("Preferred director: "),
        "actors": input("Actor(s) you like (comma-separated): ").split(","),
        "release_year": int(input("Earliest release year you want: "))
    }

    recommendations = recommend_movies(user_preferences)

    if recommendations:
        print("\nHere are some movie recommendations for you:")
        for movie in recommendations:
            print(f"- {movie['title']} ({movie['release_year']}) - Rating: {movie['rating']}")
    else:
        print("Sorry, no movies match your preferences.")

chat()
