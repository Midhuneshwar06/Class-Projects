
# Reddit API Interaction Script

## Overview
This Python script provides utilities to interact with the Reddit API using PRAW (Python Reddit API Wrapper). It includes functions to fetch top comments from a specific post and retrieve top posts from a specific Reddit user.

## Features
- **Get Top Comments**: Fetches top comments from a specified Reddit post.
- **Get User's Top Posts**: Retrieves top posts made by a specific Reddit user.

## Installation

Before running the script, ensure you have Python installed on your system. Then, install the required packages using pip:

```bash
pip install praw prawcore pandas
```

## Usage

### 1. Setup Reddit API Credentials
First, create a Reddit application to get your API credentials. You'll need the `client_id`, `client_secret`, and set a `user_agent`.

### 2. Initialize the Reddit Instance
Use your credentials to initialize the Reddit instance in the script:

```python
import praw

reddit = praw.Reddit(
    client_id='YOUR_CLIENT_ID',
    client_secret='YOUR_CLIENT_SECRET',
    user_agent='YOUR_USER_AGENT'
)
```

### 3. Using the Functions

#### Get Top Comments from a Post

```python
comments_df = get_comments(post_id="POST_ID_HERE", max_comments=10)
```

#### Get Top Posts from a User

```python
user_posts_df = get_user_posts(username="USERNAME_HERE", post_limit=5)
```

## Functions

### `get_comments(post_id, max_comments)`
Fetches and returns a DataFrame of the top `max_comments` comments from the post specified by `post_id`.

### `get_user_posts(username, post_limit)`
Retrieves and returns a DataFrame of the top `post_limit` posts made by the Reddit user `username`.

## Error Handling
The script includes error handling for scenarios such as user or post not found and general exceptions.

## Requirements
- Python 3.x
- PRAW
- pandas

## Disclaimer
This script is intended for educational purposes and should be used in accordance with Reddit's API terms and conditions.
