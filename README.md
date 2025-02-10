# UPTC News Scraper API

Welcome to the UPTC News Scraper API project! This is a Django-based REST API that scrapes and serves news data. Our core focus is to build a simple, reliable backend that:

- **Scrapes news articles** from a target website.
- **Stores** the scraped data in a database.
- **Exposes API endpoints** to serve the latest news.
- **Schedules background scraping** tasks using Celery.

We’re excited to collaborate and learn together through pair programming!

---

## Getting Started

### Prerequisites
- **Python 3.8+**
- **Git**
- **Redis** (for Celery)
- (Optional) **Virtualenv** for an isolated Python environment

### Installation

1. **Clone the Repository**
   ```bash
   git clone <REPO_URL>
   cd uptc_news_scraper_api
   ```

2. **Create & Activate a Virtual Environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # Windows: venv\Scripts\activate
   ```

3. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Apply Migrations**
   ```bash
   python manage.py migrate
   ```

5. **Run the Development Server**
   ```bash
   python manage.py runserver
   ```

6. **Start Celery Worker (in a new terminal)**
   Make sure Redis is running, then:
   ```bash
   celery -A config worker --beat --scheduler django -l info
   ```

---

## Core Features

- **Django API:** RESTful endpoints to access scraped news articles.
- **Scraping Module:** Uses `requests` and `Beautiful Soup` to fetch and parse news data.
- **Celery Integration:** Periodic tasks keep your data fresh by scraping at set intervals.

---

## How to Collaborate

- **Branching:** Create feature branches for new functionality (e.g., `feature/api-endpoints`, `feature/scraping`) and open pull requests for review.
- **Issues:** Use GitHub Issues to report bugs or propose enhancements.
- **Pair Programming:** We’re all about learning together—reach out to schedule a pair programming session if you hit a roadblock or want to work through a tricky part together.

---

## What's Next?

- Expand API endpoints and add more serializers.
- Enhance the scraper to target additional data points.
- Write tests to secure our core functionalities.

Ready to dive in? Let's build a solid foundation for the UPTC News Scraper API together!

*Happy coding and collaboration!*
