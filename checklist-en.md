## Content
 * [ ] Spell-check copy
 * [ ] Check links are correct
 * [ ] Check the website is retina compatible
 * [ ] Set favicon
 * [ ] Customize the default error views: http://bit.ly/dj-error-views 
 * [ ] Test target browsers on BrowserStack
 * [ ] Guarantee the application is mobile-friendly: http://bit.ly/ggl-mobile-friendly-tool 

## Accessibility
 * [ ] Check accessibility on Wave: http://bit.ly/wave-web-tool

## SEO & Analytics
 * [ ] Configure Google Tag Manager: http://bit.ly/tag-manager-tool 
 * [ ] Run Google Webmasters Tools: http://bit.ly/ggl-webmasters-tools  
 * [ ] Make a robots.txt
 * [ ] Make a sitemap.xml using Django
 * [ ] Check pages have descriptive and unique titles
 * [ ] Check meta descriptions are unique

## Performance
 * [ ] Check HTML, CSS and JS files are minified
 * [ ] Guarantee correct viewport `<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">`: http://bit.ly/boot-starter-template 
 * [ ] Check performance on Google Page Speed: http://bit.ly/ggl-page-speed-tool 
 * [ ] Check performance on GTmetrix: http://bit.ly/gtmetrix-tool 
 * [ ] Scan your site on webhint: http://bit.ly/webhint-tool 

## Django Settings
 * [ ] Run `python manage.py check --deploy` in production
 * [ ] Anonymize the URLs for Admin, Celery Flower, etc.
 * [ ] Check redirections, especially if it's a new platform replacing an old one
 * [ ] Properly set `ALLOWED_HOSTS`
 * [ ] Guarantee `DEBUG = False`
 * [ ] Change `SECRET_KEY`
 * [ ] Set `APPEND_SLASH = True`
 * [ ] Set `CSRF_COOKIE_SECURE = True`
 * [ ] Set `SESSION_COOKIE_SECURE = True`
 * [ ] Check `SECURE_PROXY_SSL_HEADER`, see: http://bit.ly/dj-secure-proxy-ssl-header 
 * [ ] Set `SECURE_SSL_REDIRECT = True`
 * [ ] Check if `XFrameOptionsMiddleware` is being used: http://bit.ly/dj-clickjacking-protection 
 * [ ] Set HTTP Strict Transport Security: http://bit.ly/dj-http-strict-transport-security 
 * [ ] Set `SECURE_CONTENT_TYPE_NOSNIFF = True`
 * [ ] Set `SECURE_BROWSER_XSS_FILTER = True`
 * [ ] If using subdomains, set `SESSION_COOKIE_DOMAIN`: http://bit.ly/dj-session-security 
 * [ ] Set and test `ADMINS` for 500 errors emails
 * [ ] Set and test `MANAGERS` for 404 errors emails
 * [ ] Check CORS settings, use https://github.com/ottoyiu/django-cors-headers
 * [ ] Consider `ATOMIC_REQUESTS` to assert DB integrity: http://bit.ly/dj-database-transactions 
 * [ ] Set `upload_to` argument for all `FileField` and `ImageField`
 * [ ] Use environment variables, not hardcoded settings

## Transactional Emails
 * [ ] Check if `DEFAULT_FROM_EMAIL` is set to a friendly reply email
 * [ ] Check if email templates are correct
 * [ ] Configure SendGrid, Mailgun, or another transactional email service
 * [ ] Set an automatic BCC on SendGrid
 * [ ] Save metadata of every email sent, use http://bit.ly/anymail-signals 

 ## Monitoring
 * [ ] Check no sensitive data is being logged
 * [ ] Check if logs are prefixed according to task/feature
 * [ ] Configure Papertrail or another logging service


 * [ ] Set Papertrail alerts and integrate with Slack and email  
 * [ ] Configure Sentry for backend, including Celery
 * [ ] Configure Sentry for frontend
 * [ ] Configure Uptime Robot
 * [ ] Configure New Relic

## Security
 * [ ] Check the SaaS CTO Security Checklist: http://bit.ly/sqreen-security-checklist 
 * [ ] Run Observatory: http://bit.ly/mozilla-observatory 
 * [ ] Add all accesses of third-party tools to LastPass or another password manager service
 * [ ] Update OAuth callback/deauthorize URLs in all third-party services
 * [ ] Rotate OAuth keys of all third-party services
 * [ ] Change passwords of all third-party services
 * [ ] Check if buckets/blob storages of AWS/Azure are private
 * [ ] Setup AWS S3 buckets encryption
 * [ ] Set Django shell to be read-only

## DNS
 * [ ] Check records
 * [ ] Check TTL, set low when launching, set high after everything is fine
 * [ ] [Heroku] Add a custom domain: http://bit.ly/heroku-custom-domain 
 * [ ] Move API to a different subdomain (like `api.example.org`), this allows a different server for frontend
 * [ ] Enforce or remove www subdomain (and set `PREPEND_WWW` in Django if necessary)

## Server
 * [ ] [Heroku] Check if latest stack is being used
 * [ ] Check if latest server OS version is being used
 * [ ] Check if latest server Python version is being used
 * [ ] Configure Redis maxmemory and eviction policy (likely `volatile-ttl`)
 * [ ] Configure RabbitMQ: http://bit.ly/rabbitmq-production-checklist 
 * [ ] Configure SSL for everything
 * [ ] Test SSL health: http://bit.ly/ssl-server-test 
 * [ ] Configure SSL certificates autorenewal
 * [ ] [Heroku] Set a "Standard" database or higher
 * [ ] Tune PostgreSQL settings: http://bit.ly/pgtune-tool 
 * [ ] Configure database backups generation scripts
 * [ ] Configure entire database server disk backup
 * [ ] Guarantee Celery and other services aren't running as sudo
 * [ ] Configure application firewall for application servers
 * [ ] Limit file size for uploads
 * [ ] Validate uploads media types: http://bit.ly/dj-validating-file-types 
 * [ ] Configure throttling
 * [ ] Configure autoscaling
 * [ ] Enable HTTP/2
 * [ ] Check if all services are able to handle autoscaling upper limits. (Eg.: will your Redis be able to handle connections if X servers are provisioned)
 * [ ] Configure Cloudflare DNS/caching 
	 * [ ] Enable Brotli Compression
	 * [ ] Check and enable the speed features that don't interfere with your application
 * [ ] Enable other speed/WAF features if you have a paid plan
