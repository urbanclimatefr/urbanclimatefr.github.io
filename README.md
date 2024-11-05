# Kenneth T. Y. Chung - Data Engineer 

## Certifications

- [Microsoft Certified: Azure Data Engineer Associate](https://learn.microsoft.com/en-us/users/tinyuetchung/credentials/b7951cf08bfe19e2)
- [Databricks Certified Data Engineer Associate](https://credentials.databricks.com/123b127a-7f20-43ef-a6fb-343b63b66364)
- [Microsoft Certified: Azure Data Scientist Associate](https://learn.microsoft.com/en-us/users/tinyuetchung/credentials/4de0380e29e35b8c))
- [dbt Fundamentals](https://credentials.getdbt.com/5cdefa5e-94df-4761-8019-9b5bf4bacd15#acc.fOYQKS0u)
---

### Under the Hood

This site is made with [Jekyll](https://jekyllrb.com), an open source static site generator. This means the Jekyll program takes the content we want to be on the site and turns them into HTML files ready to be hosted somewhere. Awesomely, GitHub provides free web hosting for repositories, called [GitHub Pages](https://pages.github.com/), and that's how this site is hosted. The content for the site is on a branch named [gh-pages](https://github.com/github/government.github.com/tree/gh-pages).

## Contributing

#### Fix/Edit Content

If you see an error or a place where content should be updated or improved, just fork this repository to your account, make the change you'd like and then submit a pull request. If you're not able to make the change, file an [issue](https://github.com/github/government.github.com/issues/new).

#### Add Organization

If you know of an [GitHub organization](https://help.github.com/articles/about-organizations/) that should be added to the organization list that generates the matrix of avatars on the [Community](https://government.github.com/community/) page: fork this repository, open the [_data/civic_hackers.yml](_data/civic_hackers.yml), [_data/governments.yml](_data/governments.yml), or[_data/research.yml](_data/research.yml) file and add it to the appropriate section of the list in the format being used. Commit your change and submit a pull request to us!

---

## To Set up Locally

You can take all the files of this site and run them just on your computer as if it were live online, only it's just on your machine.

#### Requirements

* [Jekyll](https://jekyllrb.com/)
* [Ruby](https://www.ruby-lang.org/en/)
* [Git](https://git-scm.com/)
* A JavaScript runtime ([node.js](https://nodejs.org/en))

_If you have installed [GitHub Desktop](https://desktop.github.com), Git was also installed automatically._

To copy the repository's files from here onto your computer and to view and serve those files locally, at your computer's command line type:

```bash
git clone https://github.com/github/government.github.com.git
cd government.github.com
script/bootstrap
script/server
```
Open `http://localhost:4000` in your browser

## Deploying

government.github.com now utilizes a two-repo approach to managing staging and production deployments:

- **Production:** [github/government.github.com](https://github.com/github/government.github.com/) (this repository)
- **Staging:** [government/staging](https://ghe.io/government/staging)

For small changes, you can deploy right to production by merging a pull request. For larger changes, push your branch to the staging repo from Terminal. Here's how to setup staging and deploy to it:

```
$ script/stage staging
```


This script will generate the government site (without starting the local server) and prep it for staging. It does this by creating a temporary Git repo within the compiled `_site` directory and force pushing that to a separate remote repo (in this case, https://ghe.io/government/staging).

Pushing to the staging repo requires authenticating with GitHub via Terminal. You'll be asked for a username and password when running `script/stage`. Use your GHE.io username and, since we enforce 2FA, use a [personal access token](https://help.github.com/articles/creating-a-personal-access-token-for-the-command-line/) as your password.

_Having trouble deploying to a staging server? Delete the entire `_site` directory and try again. Sometimes the temporary Git repository we make in the script can go awry._

When you're done with staging and your pull request has been approved, you can merge your branch. Your changes will be automatically deployed to the production site in a few minutes.

----

