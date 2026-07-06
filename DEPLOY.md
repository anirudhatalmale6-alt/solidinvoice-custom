# SolidInvoice Custom Deployment - Top Trading 2023

## What's included
- SolidInvoice 3.0.1 with all customizations
- WhatsApp share button on invoices
- Tally Excel stock importer
- English locale (currency/country)
- Email optional, phone required
- Branding removed
- Delete options removed (cancel/archive only)
- Logo sizing fixed

## Deployment Steps (cPanel Shared Hosting)

### 1. Download the ZIP
Download `solidinvoice-custom.zip` from the Releases section.

### 2. Upload via cPanel File Manager
- Login to cPanel
- Open File Manager
- Navigate to `public_html/invoice` (or create it)
- Click Upload and upload the ZIP
- Right-click the ZIP and select Extract
- Move files from `si-release/` to the current directory

### 3. Set permissions
Via cPanel Terminal or File Manager:
- `var/` directory: 777 or 775
- `.env` file: 644

### 4. Create Database
- In cPanel, go to MySQL Databases
- Create a new database (e.g., `salononl_invoice`)
- Create a user and assign all privileges
- Note the database name, username, and password

### 5. Run Setup
- Visit `https://yourdomain.com/invoice/setup-check.php`
- Verify all checks pass
- Visit `https://yourdomain.com/invoice/`
- Follow the installation wizard
- Enter database credentials when prompted

### 6. Tally Stock Importer
- Visit `https://yourdomain.com/invoice/tools/tally-importer.php`
- Upload your Tally Excel export

## Requirements
- PHP 8.2+ (8.4 recommended)
- MySQL 8.0+ or MariaDB 10.6+
- PHP extensions: curl, gd, intl, openssl, pdo_mysql, mbstring, zip, xml
