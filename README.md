# Jekyll + Netlify CMS

This is the basic Jekyll starter site, with Netlify CMS integrated.

## Getting Started

Then open a new terminal, `cd` into your new repo and run:

```bash
git clone https://github.com/tax1/jekyll/
cd jekyll
bundle install
bundle exec jekyll build
bundle exec jekyll server --watch
```

Now navigate to [localhost:4000](http://localhost:4000/) to preview the site, and
to [localhost:4000/admin](http://localhost:4000/admin) to log into the CMS.

## Deploying to production

To deploy to production, make sure to push this repository to a Github repo you own.

Then go to [netlify](https://app.netlify.com) and start a new project. Pick your
new Github repository. Netlify should fill out the build command and public folder
(`jekyll build` and `/_site`).

Build and deploy the site.

Now go to [the GitHub developer application screen](https://github.com/settings/developers)
and **register new application**.

Once you've setup the application, go back to netlify, navigate to the **Access** tab. Then
fill in your new Client ID and Client Secret in the Github Authentication Provider and check
the **Enable GitHub** box.

Now anybody with write access to your GitHub repository can log in at yoursite.netlify.com/admin
and use the CMS.

You need to Modify /admin/config.yml

  
  ```bash
cd jekyll/admin/
leafpad config.yml

```

Change Path to your Github repository && Change with you Netlify Webtite url :

  repo: tax1/jekyll # Change Path to your Github repository
  netlify.configure({'site_id': YourSite.netlify.com}); # Change with you name site on Netlify


**Enjoy!**

## Bug reports, feature requests, etc

Help to configure :

https://www.netlify.com/docs/authentication-providers/#using-an-authentication-provider
https://www.netlify.com/blog/2015/10/28/a-step-by-step-guide-jekyll-3.0-on-netlify/

We love feedback, contributions, better documentation, tutorials, general comments,
random hatemail, rants, love, crazy ideas, etc, etc!

Contact us at [any of netlify's normal channels](https://www.netlify.com/contact) and
open issues or pull requests at [the netlify-cms GitHub repo](https://github.com/netlify/netlify-cms)
