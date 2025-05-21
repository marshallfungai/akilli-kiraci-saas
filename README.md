# Akilli Kiraci SaaS

A Laravel-based SaaS application for property and tenant management.

## Features
- **Property Management**: Track properties, units, and maintenance requests.
- **Tenant Portal**: Tenants can submit requests, pay rent, and communicate.
- **Multi-language Support**: Supports multiple languages (English, Arabic, Spanish, etc.).
- **Payment Integration**: Stripe and PayPal for seamless transactions.
- **Admin Dashboard**: Manage users, roles, permissions, and system settings.

## Technology Stack
- **Backend**: Laravel (PHP)
- **Frontend**: Blade templates, Tailwind CSS
- **Database**: MySQL
- **Deployment**: AWS Elastic Beanstalk

## Setup
1. Clone the repository:
   ```bash
   git clone <repository-url>
   ```
2. Install dependencies:
   ```bash
   composer install
   npm install
   ```
3. Configure `.env`:
   ```bash
   cp .env.example .env
   php artisan key:generate
   ```
4. Run migrations and seeders:
   ```bash
   php artisan migrate --seed
   ```

## Deployment
Deployed on AWS Elastic Beanstalk with the following configurations:
- Nginx for web server.
- PHP-FPM for PHP processing.
- Environment variables configured via Elastic Beanstalk console.

## Support
For issues or questions, contact the development team.
