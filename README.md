# Wordpress-Malware-Fix
The guide to fix majority of malware and virus attacks on Wordpress Websites/Blogs.

# Resolving the Malware/Virus
Step to follow:
1. Open https://sitecheck.sucuri.net and enter your wordpress website URL in the input box. (Or go to Step 2)
2. Install Sucuri Plugin from Wordpress dashboard.
3. The tool mentioned above will give you a report if any of the core Wordpress files were edited or added.
4. Take a backup of those files from your server and then delete those files. In most cases, this shouldn't effect your website at all. If    it does effect, roll-back the changes and then delete those files one-after-another and keep checking if it effects/hurts the website in    any way.
5. This should solve the problem in majority of the cases. But if the site had a Javascript injection, then follow the steps below too.
6. Open the website http://www.unmaskparasites.com and enter your WordPress Website URL.
7. This will give you a list of all external links that your side is pointing towards.
8. Find the links which are malicious copy the links and find them in the files mentioned below.
    index.php in root folder
    wp-config.php in root folder
    index.php in wp-admin folder
    header.php in wp-admin folder
    index.php in wp-contents/yourtheme_folder
    header.php in wp-contents/yourtheme_folder
    default-filters.php in wp-includes folder
9. Delete those scripts from the files.
10. Go back to your browser and hit [CTRL+F5] to refresh with cache clear or you can just clear the cache and reload the page. And all your     malware issues should be resolved.

# Adding Additional Layers of Security for future protection
1. Majority of these attacks happen due to XSS, so the first step should be to resolve that issue.
2. Add the line mentioned below to your .htaccess file which you can find in your project root.


   Header set X-XSS-Protection "1; mode=block"

3. Now add CDN to protect the website from DDoS attacks and login attacks. You can use CloudFlare which is free and does a really good job.    You can find resources on how to implement CloudFlare easliy with a Google Search.
4. Add Website Firewall, you can use either CloudFlare or Sucuri for that. [Paid Tools]
5. Change all passwords for your cloud service provider or hosting company.
6. Change passwords and also login URLs for Wordpress website.

# Backup the Wordpress Website/Blog
1. Now that your website is safe and stable. Take a backup of it so that in case of any future issues, you can always restore a stable version of your website in a easy way.
2. I recommend using UpdraftPlus, its easy to use and is pretty self explainatory. 

That's it! Follow these steps and you should be back to a stable and fully functional Wordpress website.
