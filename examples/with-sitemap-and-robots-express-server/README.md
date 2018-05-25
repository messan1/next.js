[![Deploy to now](https://deploy.now.sh/static/button.svg)](https://deploy.now.sh/?repo=https://github.com/zeit/next.js/tree/master/examples/with-sitemap-and-robots)

# Example with sitemap.xml and robots.txt using Express server

## How to use

### Using `create-next-app`

Execute [`create-next-app`](https://github.com/segmentio/create-next-app) with [Yarn](https://yarnpkg.com/lang/en/docs/cli/create/) or [npx](https://github.com/zkat/npx#readme) to bootstrap the example:

```bash
npx create-next-app --example with-sitemap-and-robots-express-server with-sitemap-and-robots-express-server-app
# or
yarn create next-app --example with-sitemap-and-robots-express-server with-sitemap-and-robots-express-server-app
```

### Download manually

Download the example [or clone the repo](https://github.com/zeit/next.js):

```bash
curl https://codeload.github.com/zeit/next.js/tar.gz/canary | tar -xz --strip=2 next.js-canary/examples/with-sitemap-and-robots-expres-server
cd with-sitemap-and-robots-express-server
```

Install it and run:

```bash
npm install
npm run dev
# or
yarn
yarn dev
```

Deploy it to the cloud with [now](https://zeit.co/now) ([download](https://zeit.co/download))

```bash
now
```

## The idea behind the example

This example app shows you how to set up sitemap.xml and robots.txt files for proper indexing by search engine bots.

The app is deployed at: https://sitemap-robots.now.sh. Open the page and click the links to see sitemap.xml and robots.txt. Here is a snapshot of these files, with sitemap.xml on the left and robots.txt on the right:
![sitemap-robots](https://user-images.githubusercontent.com/26158226/38786210-4d0c3f70-40db-11e8-8e44-b2c90cfd1b74.png)

Notes:
- routes `/a` and `/b` are added to sitemap manually
- routes that start with `/posts` are added automatically to sitemap; in a real application, you will get post slugs from a database

When you start this example locally:
- your app with run at https://localhost:8000
- sitemap.xml will be located at http://localhost:8000/sitemap.xml
- robots.txt will be located at http://localhost:8000/robots.txt

In case you want to deploy this example, replace the URL in the following locations with your own domain:
- `hostname` in `server/sitemapAndRobots.js`
- `ROOT_URL` in `server/app.js`
- `Sitemap` at the bottom of `robots.txt`
- `alias` in `now.json`

Deploy with `now` or with `yarn now` if you specified `alias` in `now.json`