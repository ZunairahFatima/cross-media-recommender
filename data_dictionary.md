
# Cross-Media Recommendation System
## Data Dictionary

### 1. Project Objective

The objective of this project is to develop a content-based recommendation system that connects books and movies based on their themes, genres, and story descriptions.

The system will recommend movies based on books a user likes, and books based on movies a user likes.

### 2. Feature Categories

**Core Identification**
- item_id
- title
- media_type
- creator
- year

**Recommendation Features**
- themes
- genres
- description

**Supporting Features**
- rating
- language
- popularity

**Display and Data Management**
- image_url
- item_url
- source
- source_id

### 3. Data Types and Definitions

| Column | Data Type | Required? | Purpose |
|---|---|---|---|
| item_id | String | Yes | Unique identifier |
| title | String | Yes | Title of the work |
| media_type | String | Yes | Book or movie |
| creator | String | Preferred | Author or director |
| year | Integer | No | Publication or release year |
| genres | List | Preferred | Genres associated with the work |
| themes | List | Preferred | Underlying themes |
| description | String | Preferred | Story synopsis |
| rating | Float | No | Audience rating |
| language | String | No | Language of the work |
| popularity | Numeric | No | Popularity measure |
| image_url | String (URL) | Preferred | Book cover or movie poster |
| item_url | String (URL) | No | Link to information about the work |
| source | String | Yes | Origin of the record |
| source_id | String | Yes | Original API identifier |

### 4. Missing-Value Policy

- Missing titles and media types will not be accepted.
- Missing themes and genres will be investigated.
- Missing descriptions will be recorded and evaluated.
- Missing ratings will remain missing rather than being replaced with zero.
- Missing image URLs will be allowed.
- We will not invent missing information.

### 5. Recommendation Feature Priorities

Our initial experimental feature weights are:

| Feature | Weight |
|---|---:|
| Themes | 40% |
| Genres | 30% |
| Description | 25% |
| Other features | 5% |
| **Total** | **100%** |

These weights are initial hypotheses and will be evaluated and adjusted during model development.
