# Reddit Comment and Post Extractor

A Tampermonkey userscript that extracts Reddit comments and posts into a structured JSON format with configurable filters.

## Features
- Extract both posts and comments
- Configurable filters:
  - Minimum votes per comment
  - Maximum comment nesting depth
- Selective data inclusion
- Multiple output options
- Compatible with both old and new Reddit interfaces

## Installation
1. Install a userscript manager
2. [Click here to install the script](https://raw.githubusercontent.com/anassk01/redditCommentExtractor/refs/heads/master/redditCommentExtractor.script.js)

## Usage
1. Navigate to any Reddit post
2. Click Tampermonkey icon > "Extract Reddit Comments"
3. Configure settings and extract data

## JSON Structure Example

```json
{
  "metadata": {
    "extractionDate": "2023-07-20T12:34:56.789Z",
    "totalComments": 42,
    "postTitle": "Sample Post Title",
    "subreddit": "askscience",
    "criteria": {
      "minVotes": 5,
      "maxDepth": 4
    }
  },
  "post": {
    "content": "Full post text...",
    "author": "ScienceFan123"
  },
  "comments": [
    {
      "content": "Top-level comment...",
      "depth": 0,
      "votes": 123,
      "username": "User123",
      "date": "2023-07-19T15:30:00",
      "profileUrl": "/user/User123",
      "permalink": "/r/askscience/comments/12345/..."
    }
  ]
}
```

## Configuration Options
| Setting | Description | Default |
|---------|-------------|---------|
| Minimum Votes | Comments vote threshold | 1 |
| Maximum Depth | Comment nesting limit | 4 |

## License
MIT License - see [LICENSE](LICENSE)

---
*Unofficial tool - Follow Reddit's [API Rules](https://www.reddit.com/wiki/api)*
