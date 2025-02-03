## SnoopStats - Social Media Competitor Analysis Tool: Track Metrics Like Likes, Views, and Shares

### Overview
The Django-based service now focuses on monitoring competitors' activity using metrics like likes, views, comments, and shares from competitors' websites and social media platforms.

### Features
- Scraping competitor data: Collecting data on likes, views, comments, and shares from competitors' websites and social media.
- Storing data in a database: All collected metrics are saved in the database (PostgreSQL or SQLite).
- Subscription system: Users can subscribe to competitors and track data on likes, views, comments, and shares.
- User dashboard: Users can see how their competitors' metrics are changing, track popular posts, and receive notifications about significant changes.

### Pages and Features:
1. Landing Page:
- Basic information about the service with options to register or log in.
- Buttons for registration and login.

2. Login/Registration:
- Users can register or log in to start tracking competitors and receiving notifications.

3. Dashboard/Newsfeed:
- The main page after login.
- Displays updates from competitors, tracked through likes, views, comments, and shares.
- Users can filter data based on these metrics to monitor which competitor posts are receiving the most attention.

4. Personal Page:
- A personal page for users to manage subscriptions to competitors.
- Displays data on likes, views, comments, and shares for each competitor.

### Detailed Features to Integrate:
1. Scraping likes, views, comments, and shares:
- Use BeautifulSoup for scraping social metrics from competitors' websites and social media platforms.
- For social media, APIs (such as Facebook API, Instagram API, YouTube API) can be used to retrieve likes, views, comments, and shares.
- The collected data should be stored in the database for later analysis.

2. Database Models:
- Competitor: Name, URL, social media profiles, description.
- SocialMetrics: Competitor ID, likes, views, comments, shares, content type (e.g., Facebook post, YouTube video), timestamp of data collection.
- UserSubscriptions: User ID, Competitor ID, subscription status.
- Notifications: User ID, Competitor ID, notification content.

3. Subscriptions and Notifications:
- Users can subscribe to competitors and track changes in likes, views, comments, and shares.
- Use Django signals or background tasks (e.g., Celery) to notify users when a competitor's metrics change (e.g., when a post receives more likes or shares).

4. Dashboard:
- The dashboard will display competitor metrics: likes, views, comments, and shares.
- Users can view updates for each competitor and track which posts or pages are receiving the most attention.
- Visualization of data using graphs and charts to make it easier for users to analyze trends.

5. Search:
- Implement a search feature so users can search for competitors or specific posts based on metrics (e.g., "most popular post" based on likes).

6. Footer:
- Site Information: Including when the site was created, contact details, etc.

### Installation
- Prerequisites
- Python 3.x
- Django
- PostgreSQL or SQLite (default)
- Playwright for web scraping
- Social Media APIs (such as Facebook, Instagram, YouTube APIs)

