# Cannot use Workers Secrets in Webpack project

This repository contains code that I use to reproduce the error when using
Cloudflare Workers Secrets in webpack project.

Step by step to reproduce:

    git clone https://github.com/pyk/cf-worker-secrets-test.git
    cd with-webpack/

Rename the `wrangler.toml.example` to `wrangler.toml` and update `YOUR_ACCOUNT_ID` and `YOUR_ZONE_ID`.

Create the secret using the following command:

    wrangler secret put MY_SECRET

Then publish the worker:

    wrangler publish

Access `https://cf-worker-secrets-test-with-webpack.YOURNAME.workers.dev`.

You should see an error.

Where project [without webpack](./without-webpack) runs fine.
