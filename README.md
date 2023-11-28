# moviesRecomnder
Uses the vector Method to assign the tags and than utilize Cosine to find the nearest VEctor among the words to find the TOP 10 recomneded movie 
# Movie Recommendation System

This project implements a movie recommendation system using machine learning techniques, specifically utilizing the cosine similarity classification algorithm provided by the scikit-learn (sklearn) library. The recommendation system searches through movie vectors to provide personalized suggestions based on user preferences.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Dependencies](#dependencies)
- [Contributing](#contributing)
- [License](#license)

## Introduction

Movie recommendation systems have become an integral part of streaming platforms, helping users discover new content tailored to their tastes. This project focuses on building a recommendation system that employs the cosine similarity algorithm to find similarities between movies and recommend those that are likely to be enjoyed by the user.

## Features

- **Cosine Similarity:** Utilizes the cosine similarity classification algorithm to determine the similarity between movies.
- **Vectorized Representation:** Represents movies as vectors to efficiently calculate the cosine similarity.
- **Personalized Recommendations:** Generates personalized movie recommendations based on user preferences.
- **Scikit-learn Integration:** Leverages the scikit-learn library for machine learning functionalities.


    ```

## Usage

1. Prepare your movie dataset in a compatible format (e.g., CSV, JSON).
2. Run the preprocessing script to convert the dataset into a format suitable for the recommendation system:

    ```bash
    python preprocess.py --input_path /path/to/your/dataset.csv --output_path processed_dataset.pkl
    ```

3. Train the recommendation system:

    ```bash
    python train.py --input_path processed_dataset.pkl --model_path recommendation_model.pkl
    ```

4. Use the trained model to get movie recommendations:

    ```python
    from recommend import MovieRecommendationSystem

    model = MovieRecommendationSystem.load_model('recommendation_model.pkl')

    user_preferences = {
        'movie_id_1': rating_1,
        'movie_id_2': rating_2,
        # Add more movie ratings as needed
    }

    recommendations = model.get_recommendations(user_preferences, top_n=5)
    print("Recommended Movies:", recommendations)
    ```

## Dependencies

- Python 3.x
- scikit-learn
- pandas
- numpy

Install dependencies using:

```bash
pip install scikit-learn pandas numpy
```

## Contributing

Contributions are welcome! Feel free to open issues or pull requests.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
