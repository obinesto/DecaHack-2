# `DecaHack2`

Welcome to your new `DecaHack2` project and to the Internet Computer development community. By default, creating a new project adds this README and some template files to your project directory. You can edit these template files to customize your project and to include your own code to speed up the development cycle.

To get started, you might want to explore the project directory structure and the default configuration file. Working with this project in your development environment will not affect any production deployment or identity tokens.

To learn more before you start working with `DecaHack2`, see the following documentation available online:

- [Quick Start](https://internetcomputer.org/docs/current/developer-docs/setup/deploy-locally)
- [SDK Developer Tools](https://internetcomputer.org/docs/current/developer-docs/setup/install)
- [Motoko Programming Language Guide](https://internetcomputer.org/docs/current/motoko/main/motoko)
- [Motoko Language Quick Reference](https://internetcomputer.org/docs/current/motoko/main/language-manual)

If you want to start working on your project right away, you might want to try the following commands:

```bash
cd DecaHack2/
dfx help
dfx canister --help
```

## Running the project locally

If you want to test your project locally, you can use the following commands:

```bash
# Starts the replica, running in the background
dfx start --background

# Deploys your canisters to the replica and generates your candid interface
dfx deploy
```

Once the job completes, your application will be available at `http://localhost:4943?canisterId={asset_canister_id}`.

If you have made changes to your backend canister, you can generate a new candid interface with

```bash
npm run generate
```

at any time. This is recommended before starting the frontend development server, and will be run automatically any time you run `dfx deploy`.

If you are making frontend changes, you can start a development server with

```bash
npm start
```

Which will start a server at `http://localhost:8080`, proxying API requests to the replica at port 4943.

### Note on frontend environment variables

If you are hosting frontend code somewhere without using DFX, you may need to make one of the following adjustments to ensure your project does not fetch the root key in production:

- set`DFX_NETWORK` to `ic` if you are using Webpack
- use your own preferred method to replace `process.env.DFX_NETWORK` in the autogenerated declarations
  - Setting `canisters -> {asset_canister_id} -> declarations -> env_override to a string` in `dfx.json` will replace `process.env.DFX_NETWORK` with the string in the autogenerated declarations
- Write your own `createActor` constructor


```
DecaHack2
├─ .git
│  ├─ COMMIT_EDITMSG
│  ├─ FETCH_HEAD
│  ├─ HEAD
│  ├─ branches
│  ├─ config
│  ├─ description
│  ├─ hooks
│  │  ├─ applypatch-msg.sample
│  │  ├─ commit-msg.sample
│  │  ├─ fsmonitor-watchman.sample
│  │  ├─ post-update.sample
│  │  ├─ pre-applypatch.sample
│  │  ├─ pre-commit.sample
│  │  ├─ pre-merge-commit.sample
│  │  ├─ pre-push.sample
│  │  ├─ pre-rebase.sample
│  │  ├─ pre-receive.sample
│  │  ├─ prepare-commit-msg.sample
│  │  ├─ push-to-checkout.sample
│  │  └─ update.sample
│  ├─ index
│  ├─ info
│  │  └─ exclude
│  ├─ logs
│  │  ├─ HEAD
│  │  └─ refs
│  │     ├─ heads
│  │     │  └─ master
│  │     └─ remotes
│  │        └─ origin
│  │           └─ master
│  ├─ objects
│  │  ├─ 11
│  │  │  └─ f02fe2a0061d6e6e1f271b21da95423b448b32
│  │  ├─ 17
│  │  │  └─ 3e7221c5a490481163bd5eb11da4888a3ff6b9
│  │  ├─ 1d
│  │  │  └─ a0a27e3622f6e2b013424ffdbb50c654e41743
│  │  ├─ 33
│  │  │  ├─ 4e63809a9f49b53706b9b279d1abcaac3a6ce5
│  │  │  └─ 8fbf34cd80a1fd7d0c259aae42b566a56f7168
│  │  ├─ 39
│  │  │  └─ a545e919b81c6fb83bf7f9fcbd2a4d29b7dad8
│  │  ├─ 41
│  │  │  └─ 70aeb389e875ecbacff110ffe1998ddf5a9633
│  │  ├─ 45
│  │  │  └─ e2be5437701d52072ebb535e7f8d5d6da5e567
│  │  ├─ 49
│  │  │  ├─ b2aaf3fd5047aa47f5d7f281f51d4ce416277e
│  │  │  └─ c89a1c9583641168a0ac523f3686b9e3e1477a
│  │  ├─ 4a
│  │  │  └─ fee5f370c79c8a6ba034e16df4083a4f05ca27
│  │  ├─ 51
│  │  │  └─ b65e147dac4158f083c0ccb571dd3a8ea3e8ed
│  │  ├─ 54
│  │  │  └─ 0f30b98dbfbdabca3d8aa2c9506c5614a133e0
│  │  ├─ 5a
│  │  │  └─ 027e845b036cc70afe82f5cf027feccc3f98da
│  │  ├─ 67
│  │  │  └─ 0b0347b6057301e278df02b8d581f6fa9ed4eb
│  │  ├─ 74
│  │  │  └─ bc67e39d98f3342d408b398ffee140061ac59d
│  │  ├─ 7f
│  │  │  └─ 7e653dbadbc8ceb60df96e0c971017334f816d
│  │  ├─ 8f
│  │  │  └─ a676cca944da0e8b110bbe0dbcb95b4f19a9c2
│  │  ├─ 92
│  │  │  └─ 6fbf9232bc3c9b6f6708024a5346020bbb8fe2
│  │  ├─ 9d
│  │  │  └─ d90338a514c2fac90a6b3c0b6c2f39d1f62b7b
│  │  ├─ 9e
│  │  │  └─ c78c35d291a980b7960445d3153e03ddb49e83
│  │  ├─ a8
│  │  │  └─ f14f76b865f608aa7769cb89db555733f0a545
│  │  ├─ c1
│  │  │  └─ c320834c3323220e783284bfef0ff85948e3c6
│  │  ├─ d7
│  │  │  └─ 06e89a3ed1bee9a5f412aa186170243b0ded70
│  │  ├─ ed
│  │  │  └─ 81321587e57e8aa6291f473ed2b6fb6a91f6cf
│  │  ├─ f0
│  │  │  └─ 5a798c37c5bcddaed412810d25d111f0fec247
│  │  ├─ f1
│  │  │  └─ 1d23b5cd6c04c3addf0344345e3b4d9d5ee932
│  │  ├─ f4
│  │  │  └─ 629166d90f19e24c2bbc42c1090b01d4b8fe02
│  │  ├─ info
│  │  └─ pack
│  └─ refs
│     ├─ heads
│     │  └─ master
│     ├─ remotes
│     │  └─ origin
│     │     └─ master
│     └─ tags
├─ .gitignore
├─ README.md
├─ dfx.json
├─ package-lock.json
├─ package.json
├─ src
│  ├─ DecaHack2_backend
│  │  ├─ landing.mo
│  │  ├─ login.mo
│  │  └─ signup.mo
│  ├─ DecaHack2_frontend
│  │  ├─ index.html
│  │  ├─ package.json
│  │  ├─ public
│  │  │  ├─ .ic-assets.json5
│  │  │  ├─ favicon.ico
│  │  │  └─ logo2.svg
│  │  ├─ src
│  │  │  ├─ App.jsx
│  │  │  ├─ components
│  │  │  ├─ index.css
│  │  │  ├─ main.jsx
│  │  │  └─ vite-env.d.ts
│  │  ├─ tsconfig.json
│  │  └─ vite.config.js
│  └─ declarations
│     ├─ DecaHack2_backend
│     │  ├─ DecaHack2_backend.did
│     │  ├─ DecaHack2_backend.did.d.ts
│     │  ├─ DecaHack2_backend.did.js
│     │  ├─ index.d.ts
│     │  └─ index.js
│     └─ DecaHack2_frontend
│        ├─ DecaHack2_frontend.did
│        ├─ DecaHack2_frontend.did.d.ts
│        ├─ DecaHack2_frontend.did.js
│        ├─ index.d.ts
│        └─ index.js
└─ tsconfig.json

```