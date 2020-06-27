Test secret, make sure it is accessible.

Create the secret using the following command:

    wrangler secret put MY_SECRET

Then publish the worker:

    wrangler publish

Access `https://cf-worker-secrets-test-with-webpack.YOURNAME.workers.dev`.
