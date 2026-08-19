# Sprout Share — Plant Rental Service
 
A full-stack Django marketplace for renting houseplants, built as the team project for UVA's CS 3240 (Software Engineering), Spring 2025.
 
**Live demo:** https://project-b-25-swe-ae2999597b7a.herokuapp.com/
*(Class project — not actively monitored; please don't submit real personal information.)*
 
## Overview
 
Sprout Share lets users browse, filter, and rent plants from other members of the community. Owners list plants with care details and photos; renters can search by care requirements and budget, view listings, and leave reviews.
 
## Features
 
- **Google OAuth sign-in** — account creation and login handled via Google, no password storage
- **Browse & filter** — search the plant catalog by sunlight needs, water needs, humidity, size, difficulty, and price range
- **Listing details** — each plant has a description, location, care profile, price, and owning "sherriff" (steward)
- **Reviews & ratings** — renters can leave reviews and star ratings on individual plants
- **Image storage** — plant photos are stored and served from Amazon S3
- **Role-based access control** — distinct permissions across owner, renter, and admin user tiers
- **In-app messaging** — built-in messaging between renters and owners
- **Anonymous browsing** — the plant catalog is viewable without an account; sign-in is only required to rent
## Tech Stack
 
| Layer | Technology |
|---|---|
| Backend | Python, Django |
| Database | PostgreSQL |
| Auth | Google OAuth |
| Storage | Amazon S3 |
| Hosting | Heroku |
 
## My Role
 
I served as **Scrum Master and lead developer** for a 5-person team across 6 two-week sprints, running sprint planning, task delegation, and code review, and personally implemented the Google OAuth integration, role-based access control, and S3-backed image storage.
 
## Running Locally
 
```bash
git clone https://github.com/Jahva1229/Plant-Rental-Service-Final.git
cd Plant-Rental-Service-Final
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```
 
You'll need your own PostgreSQL instance, Google OAuth credentials, and AWS S3 credentials — set these as environment variables (see `settings.py` for the expected variable names).
 

