# aws-challenge

This is the first iteration of the AWS Challenge. A test that covers some basic AWS/Web skills and allows you to learn, and showcase your skills to the world.

## The challenge

Build a static site in AWS.

You can use your own Github Repo and AWS Account to create/test your automation.

Once you're ready you can share your github repo with me and I'll read your README.md and follow it as closely as possible to deploy your static website in our AWS Account.

I'll follow the [EXACT INSTRUCTIONS CHALLENGE](https://www.youtube.com/watch?v=Ct-lOOUqmyY) formula, so make sure your automation and instructions are rock solid!

**How to submit a solution:** Right now it's a manual process. Create your repo, and share it with me! We can run through your solution together on a video call with a screenshare. https://www.drewkhoury.com/drew/

## What you should assume

- AWS Account exists, and billing setup
- AWS role/creds for your infra exists (you need to specify the exact policy we need to use for your role, we'll handle the role and cred creation)
- Your github repo should assume the following secrets are provided `AWS_ACCESS_KEY_ID`, `AWS_SECRET_ACCESS_KEY`
- Domain already purchased in Route53, assume the following variable provided to github `DOMAIN=foo.com` (where foo.com will be a valid domain we manage)

## What your repo need to do

- Deploy a functional [Hugo website](https://gohugo.io/) (static site, no database)
- must redirect to https
- must redirect naked site to www
- must use friendly urls https://foo.com/bar (these must work without explict https://foo.com/bar/index.html)

## Suggested/guided path

No points for using EC2! We relly want to see serverless solutions.

The common approach would be a static site deployed to s3 (but not have s3 publically accessable), fronted by Cloudfront.

## How you'll be judged

- Minimum instruction/human input
- How quickly your infra takes to build
- Minimum steps/stages (we want simple and easy to understand, not "it's complex but it still works")
- Infrastructure validity/security/elegance
- How comprehensive are your tests
- Validitiy of your website (ie do the links work)
- Can you build/test site locally, with minimum assumptions (docker/make are favourable ... don't assume we have AWS CLI or Hugo installed)
- Cost to run site (how cost effective can you make it, while still being a functional and scaled website with good response times)
