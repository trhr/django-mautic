An integration to bring Mautic marketing automation into Django models

Notice: This is hacky, untested, and seems to work perfectly if you know what you're doing and set your databases up like a pro. But, seriously, back everything up if you dare try this.

# Mautic Initial Installation Changes
- Prefix database tables with with crm_
- Install Mautic inside Django MYSQL database

# Installation Instructions
- In settings.py, add 'crm' to INSTALLED_APPS
- Debug uploaded views.py; I purposefully broke it so inexperienced noobs won't wreck their site
- python manage.py makemigrations
- python manage.py migrate crm --fake

# Usage in Template/View
Used as any other django model: {{ leads.email }} {{ leads.firstname }} {{ leads.lastname }}
