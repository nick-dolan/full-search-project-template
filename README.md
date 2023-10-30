# Jesse Project Template with "Full Search" Feature

This template serves as a foundation for creating your own Jesse project, enabling a "brute force" approach to strategy optimization.

"Brute force" refers to a method where all possible configurations of a given strategy are tested to identify the optimal settings. Unlike heuristic methods, this approach relies on exhaustive computation to find the best solution based on specified criteria, without taking any shortcuts.

## Usage

Assuming you have already installed the necessary environment dependencies and imported candles, follow the steps below to create your project:

```sh
# Change "my-project" to any name you prefer
git clone https://github.com/nick-dolan/full-search-project-template my-project
# Create a .env file from the example
cp .env.example .env
```

To initiate an exhaustive search, type:

```sh
python full-search.py 
```

This setup works out-of-the-box with an example strategy from [example-strategies](https://github.com/jesse-ai/example-strategies).

The script generates all possible permutations from strategy hyperparameters. You can specify the "step" in hyperparameters; if not specified, the default step value is 0.1.

<img width="810" alt="Screenshot 2023-10-30 at 14 11 42-min" src="https://github.com/jesse-ai/project-template/assets/25667028/b5e5137e-2a6c-465c-ae4f-dd8412ed58ec">

Don't forger to set up all parameters from `.env.example`. 

Upon completion, you'll receive a .csv file containing all results along with the hyperparameters in `/storage/full-search`:

<a href="https://raw.githubusercontent.com/nick-dolan/full-search-project-template/main/full-search-example.csv">
    <img width="1389" alt="Screenshot 2023-10-30 at 14 00 10-min" src="https://github.com/jesse-ai/project-template/assets/25667028/52f27c83-8190-43f7-a094-4c648c0571f6">
</a>

To launch the standard UI, type:

```sh
jesse run
```

Now, open [localhost:9000](http://localhost:9000) in your browser to view the dashboard.

