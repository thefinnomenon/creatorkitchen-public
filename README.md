# CreatorKitchen

A retired writing and publishing prototype built in 2022. It combines a Tiptap block editor with draft previews, published revisions, author profiles, personal sites, subdomains, and custom domains.

Try the self-contained [portfolio demo](https://finnternet.com/projects/creatorkitchen/). The demo runs locally in the browser with synthetic content and illustrations; it does not contact this application’s original services.

## Source status

This is a sanitized source snapshot of `thefinnomenon/creatorkitchen` at `6b2f50706413aee796a8a1999be77143189359ec` (April 29, 2022). The original repository and its history are preserved separately. This publication starts fresh history so historical provider keys and deployment data are not carried forward. Original generated Amplify deployment identifiers have been removed.

The original application is retired and its dependencies have not been modernized. This is an archive for learning and review, not a supported production service. No existing account, backend, domain, data, or media library is included.

## Stack

- Next.js 12, React 17, TypeScript, Tailwind CSS
- Tiptap / ProseMirror with custom media, callout, audio, tooltip, and code blocks
- AWS Amplify, Cognito, AppSync GraphQL, S3
- Vercel domain APIs, Unsplash, Giphy, Iframely

## Run with your own configuration

1. Review and update the legacy dependencies for your environment. The original lockfile is `yarn.lock`.
2. Install dependencies with Yarn. Lifecycle hooks configure Husky; use `yarn install --ignore-scripts` if you only need to inspect the archive.
3. Copy `.env.example` to `.env.local` and provide settings for **your own** Amplify resources. `aws-exports.js` reads only environment variables. Never put privileged server credentials into a `NEXT_PUBLIC_` variable.
4. Provision your own Cognito user pool, AppSync API, and S3 storage. Backend schema definitions are under `amplify/backend/`; generate new deployment metadata rather than restoring old identifiers.
5. Configure any optional media or Vercel integrations with your own accounts, then run `yarn dev` at `http://localhost:3000`. Subdomain routing and custom-domain operations require additional local DNS or a separately configured deployment.

Without a configured backend, the original dashboard cannot load an authenticated author or site. The isolated portfolio demo is the easiest way to explore the editor.

## Historical limitations

The archived GraphQL schema allows public reads of content without distinguishing draft and published records. The preview, publish, and domain routes also need a fresh authorization/security review before any real deployment. Do not connect this archive to private content or an existing production backend unchanged. The archive has not been live-tested against provider services.

## License and assets

First-party source is provided under the MIT license. Third-party libraries remain under their own licenses. Existing inline attribution and third-party notices are retained. `public/vercel.svg` is a third-party brand asset and is not relicensed by this repository. No original media is used in the portfolio demo.
