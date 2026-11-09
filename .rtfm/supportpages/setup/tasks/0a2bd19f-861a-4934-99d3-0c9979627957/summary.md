# Arto (hopp-wordpress)
- Arto is a WordPress multisite publishing platform run by Oktavilla; each publication/brand has its own address and site.
- Stack: PHP/WordPress (Bedrock-style layout: web/wp core, web/app plugins, mu-plugins and one theme "hopp"), Composer, Node build for editor assets, DDEV/Docker for development.
- Single custom theme: web/app/themes/hopp (inc/ holds admin customisations, roles, rewrites, paywall, listings, newsletters, podcasts).
- Admin UI is customised in inc/clean-admin.php and inc/custom-admin.php; the login screen is WordPress core wp-login.php with the Arto logo, no language selector and Private Captcha.
- Two-factor authentication via the Two Factor plugin; force_2fa_for_admins is a per-site setting (inc/users.php).
- Plugins in web/app/plugins include a media bank (mediebank), ElasticPress search, SES mail and others.
- Users are Swedish-speaking editors and administrators (locale sv_SE).
- User-facing areas: wp-admin editing of articles, media bank, curated/featured content, listings, newsletters, podcasts, native ads, paywall and premium content.
- Tests: PHPUnit, Playwright; quality tools: phpcs, phpstan, grumphp.
