# Best AI Product Photography Tools for Ecommerce: 7 Ranked by API (2026)

This list ranks 7 AI product photography tools for ecommerce by how much of a catalogue you can process from code with nobody opening the app, using vendor docs checked in October 2026. Wireflow is first because one API call runs a whole saved product-photo workflow and can report back by webhook. Of the 7 tools, 5 publish a public API reference and 3 document a signed completion webhook.

1. **Wireflow**: Best overall for running a multi-step product photo chain from one API call, a node canvas whose saved workflows run by REST API
2. **Claid**: Best for bulk edits that start from cloud storage, an image editing API with a batch endpoint
3. **Bria**: Best for packshots from models trained on licensed data, an async API with official SDKs
4. **Photoroom**: Best for catalogues kept in a spreadsheet, a per-image API with a ready-made sheet script
5. **Pixelcut**: Best for single edits from code or an agent, a credit-priced API plus an MCP server
6. **Flair**: Best for branded scenes arranged by a designer, an editor with custom product models
7. **Pebblely**: Best for quick bulk shots from inside the app, a background generator with no public API listed

The Wireflow team maintains this list, so read entry 1 with that in mind. [Wireflow's node-based image generation page](https://www.wireflow.ai/node-based-image-generation) shows the canvas that entry 1 describes, and every other entry links to its vendor's own docs so that each cell can be checked.

The tables below are generated from [`data/tools.json`](data/tools.json) by [`scripts/update.js`](scripts/update.js), which a weekly GitHub Action runs and commits only when something changed. Every tool on this list is a hosted product with no first-party open-source repo, so there are no star counts to report. The refresh re-stamps the check date and regenerates the tables from the data.

<!-- LAST-CHECKED:START -->
Live repository data last checked **2026-10-21** by [`scripts/update.js`](scripts/update.js), which runs weekly via GitHub Actions.
<!-- LAST-CHECKED:END -->

Maintained by [a1adams](https://github.com/a1adams). Corrections are welcome, see [CONTRIBUTING.md](CONTRIBUTING.md).

## Contents

- [The data](#the-data)
- [Capability scores](#capability-scores)
- [Comparison table](#comparison-table)
- [The tools](#the-tools)
  - [Wireflow](#1-wireflow)
  - [Claid](#2-claid)
  - [Bria](#3-bria)
  - [Photoroom](#4-photoroom)
  - [Pixelcut](#5-pixelcut)
  - [Flair](#6-flair)
  - [Pebblely](#7-pebblely)
- [What each check means](#what-each-check-means)
- [How this list is maintained](#how-this-list-is-maintained)
- [FAQ](#faq)
- [Contributing](#contributing)
- [License](#license)

## The data

One row per tool, one column per thing people actually check before committing. Columns with nothing verified behind them are dropped rather than filled with guesses.

<!-- DATA-TABLE:START -->
| Tool | Claude connection | REST API | Free tier | Model support | Pricing |
|---|---|---|---|---|---|
| **[Wireflow](#1-wireflow)** | Custom connector, OAuth sign-in | Yes | [check](https://www.wireflow.ai/pricing) | 100+ image, video and audio models as nodes | [pricing](https://www.wireflow.ai/pricing) |
| **[Claid](#2-claid)** | n/a | Yes | [check](https://claid.ai/pricing) | n/a | [pricing](https://claid.ai/pricing) |
| **[Bria](#3-bria)** | MCP server | Yes | Yes | Bria models trained on licensed data | [pricing](https://bria.ai/pricing) |
| **[Photoroom](#4-photoroom)** | Custom connector in Claude | Yes | [check](https://www.photoroom.com/api/pricing) | n/a | [pricing](https://www.photoroom.com/api/pricing) |
| **[Pixelcut](#5-pixelcut)** | Custom connector (MCP) | Yes | Yes | n/a | [pricing](https://www.pixelcut.ai/api) |
| **[Flair](#6-flair)** | n/a | n/a | Yes | n/a | [pricing](https://flair.ai/pricing) |
| **[Pebblely](#7-pebblely)** | n/a | n/a | [check](https://pebblely.com/pricing/) | n/a | [pricing](https://pebblely.com/pricing/) |
<!-- DATA-TABLE:END -->

## Capability scores

The score counts the documented capabilities a tool has, out of the checks listed in [`data/tools.json`](data/tools.json) under `capabilityChecks`. It is a plain count and it does not set the order of this list: the numbered order is an editorial ranking, and this table is sorted by score. The checks and every answer are in the file, so each cell can be checked. Disagree with a cell? Open an issue naming the tool, the check and the evidence.

<!-- CAPABILITY-SCORES:START -->
| Tool | Public REST API | Async job with polling | Completion webhook | Many images in one request | Background removal | MCP server | Official SDK | Score |
|------|---|---|---|---|---|---|---|-------|
| **[Wireflow](#1-wireflow)** | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ❌ | **6/7** |
| **[Bria](#3-bria)** | ✅ | ✅ | ✅ | n/a | ✅ | ✅ | ✅ | **6/7** |
| **[Claid](#2-claid)** | ✅ | ✅ | ✅ | ✅ | ✅ | n/a | n/a | **5/7** |
| **[Photoroom](#4-photoroom)** | ✅ | ❌ | n/a | ❌ | ✅ | ✅ | n/a | **3/7** |
| **[Pixelcut](#5-pixelcut)** | ✅ | n/a | n/a | n/a | ✅ | ✅ | n/a | **3/7** |
| **[Flair](#6-flair)** | n/a | n/a | n/a | n/a | n/a | n/a | n/a | **0/7** |
| **[Pebblely](#7-pebblely)** | n/a | n/a | n/a | n/a | n/a | n/a | n/a | **0/7** |
<!-- CAPABILITY-SCORES:END -->

## Comparison table

| Tool | Best for | Pricing basis | Many products from code | Job reports back by |
|---|---|---|---|---|
| **Wireflow** | Multi-step product shots per call | Credits per generation | One run of a saved workflow | Polling or a signed webhook |
| **Claid** | Bulk edits from cloud storage | Credits per operation | Batch endpoint over a folder | Polling or a signed webhook |
| **Bria** | Packshots from licensed-data models | Per image, from $0.018 | Not published | Polling or a signed webhook |
| **Photoroom** | Catalogues kept in a spreadsheet | Per image on the API | One image per call | The HTTP response |
| **Pixelcut** | Single edits from code or MCP | API credits at $0.01 each | One operation per call | The HTTP response |
| **Flair** | Branded scenes built in an editor | Monthly plans, from $8 | API early access on Scale | Not published |
| **Pebblely** | Quick bulk shots in the app | Monthly plans, from US$9 | Bulk generate in the app | No public API listed |

Facts checked on 2026-10-11 against each vendor's own docs and pricing pages, quickstarts copied on 2026-10-21. Follow the pricing links in the data table before you buy, because prices change.

## The tools

### 1. Wireflow

*Best overall for running a multi-step product photo chain from one API call*

![Wireflow screenshot](https://assets.wireflow.ai/competitors/wireflow-70f47ccd9660.png?v=r5)

- **What it is:** [Wireflow](https://www.wireflow.ai/) is a hosted platform where ad teams and AI agents build and rerun creative on a shared node board. Each model is a node on one canvas and the output of one node feeds the next, so a product photo can pass through a cutout, an edit model with reference images and a branded layout inside one saved workflow.
- **Best for:** Ecommerce teams whose finished product image takes more than one step, for example a background removal, a new scene built from reference images and a layout in the brand's colours, and who want to start that whole chain from their own code.
- **Pricing basis:** It charges credits per generation, according to the model you run, and 1 credit is US$0.01. Starter is US$24 a month with 1,600 credits, and a model that fails is not charged. The credit price of every model is on the [Wireflow pricing page](https://www.wireflow.ai/pricing), checked October 2026.
- **Standout:** One saved workflow holds the whole treatment. The node reference lists background removal nodes (BEN2, BiRefNet, Bria and Rembg), upscalers such as Topaz and Clarity, and edit nodes that take reference images, such as FLUX 3 Image Edit with up to 10 of them. The Compositor then renders up to 50 rows per batch from one layout, and that render costs no credits. Source: [the batch image generation guide](https://www.wireflow.ai/docs/batch-image-generation).
- **Limit:** Importing a CSV file or a Google Sheet as the rows of a run is not documented, so a catalogue goes in as rows typed in the Compositor's Batch tab, a JSON array wired into its Data port, or one API call per product from your own script. There is no official SDK. The free plan lets you build up to 5 workflows, and running generations needs a paid plan.
- **API or automation:** You send a saved workflow's input values to `POST /api/v1/workflows/{id}/run`, which returns 202 with an execution ID to poll. A webhook block on the same request makes Wireflow POST the result when the run finishes, signed with HMAC-SHA256 and retried for up to 12 attempts, and a metadata object is echoed back so the result maps to your own product ID. See [the webhooks reference](https://www.wireflow.ai/docs/api/webhooks).
- **Sources:** the Wireflow homepage, pricing page, batch guide, node reference and webhooks reference, checked 2026-10-11.
- **Links:**
  - [Wireflow node based image generation page](https://www.wireflow.ai/node-based-image-generation)
  - [Docs](https://www.wireflow.ai/docs/api/overview)

Pick Wireflow when each finished product image takes more than one model call and you want the chain, the callback and the cost of each model in one place. [Wireflow's ecommerce image workflows](https://www.wireflow.ai/ai-ecommerce-images) show the kinds of scenes it is set up for. Wireflow also publishes open source Claude Code skills under the MIT license in the wireflowINC/skills repo, including one for product photography, and each skill shows the credit cost and waits for a yes before it runs. If you only need a cutout at a fixed price per image, entries 3 and 4 are simpler to call.

Add the Wireflow connector to Claude Code, from the wireflowINC/skills README. Then run /mcp to sign in.
```bash
claude mcp add --transport http wireflow https://www.wireflow.ai/api/mcp
```
Or run a saved workflow from code: send its input values to this endpoint with an API key, then poll the execution or add a webhook block. The request format is in the API reference linked under Docs.
```text
POST /api/v1/workflows/{id}/run
```

### 2. Claid

*Best for bulk edits that start from cloud storage*

![Claid screenshot](https://assets.wireflow.ai/competitors/claid-ai-b65f42ac47e8.png?v=r5)

- **What it is:** [Claid](https://claid.ai/) provides AI image editing through an API, including enhancing, resizing, background separation and colour adjustment. A separate AI Background API turns one product photo into up to 4 new scene options per request.
- **Best for:** Ecommerce teams that keep product images in cloud storage and want an API to edit a whole folder of them.
- **Pricing basis:** It charges credits per operation. Background removal costs 1 credit, and AI Photoshoot costs 4 credits at Standard quality or 10 at Studio quality. A free trial gives 50 credits, and developers can buy a dedicated API plan without a paid web plan. Plan prices are not repeated here, so see the [Claid pricing page](https://claid.ai/pricing), checked October 2026.
- **Standout:** A batch endpoint, `POST /v1/image/edit/batch`, takes a cloud storage folder or a list of public image URLs and returns before the result is ready, like the async endpoint. Storage connectors cover AWS S3, Google Cloud Storage and a web folder. Source: [Claid's batch API reference](https://docs.claid.ai/image-editing-api/batch-api-reference).
- **Limit:** The AI Background API takes one product image per request and returns 1024x1024 images, so new scenes for a catalogue are one request per product. The default rate limit is 120 requests a minute and 4 a second, and the rate limits page says to contact Claid to expand the limits or to use batch processing. Results sit in a temporary bucket for 24 hours unless you set an output folder on connected storage.
- **API or automation:** The async endpoint returns a task ID and a result URL to poll. Webhooks set in account settings send success and failed events with an optional HMAC-SHA256 signature, and each notification is tried up to 4 times with a 30-second timeout, as [the async API reference](https://docs.claid.ai/image-editing-api/async-api-reference) describes.
- **Note:** The free trial gives 50 credits. A trial is not listed here as a free tier.
- **Sources:** [Claid quick start](https://docs.claid.ai/quick-start), [Claid rate limits](https://docs.claid.ai/rate-limits) and [the AI Background API reference](https://docs.claid.ai/ai-background-api/ai-background-i-o), checked 2026-10-11 and 2026-10-21.
- **Links:**
  - [Docs](https://docs.claid.ai/)

Pick Claid over Wireflow when the job is one edit applied to thousands of files that already sit in a bucket, and you do not need several models chained per image. Ask Claid about batch limits before a large run, because its rate limits page routes batch processing through a conversation with them.

Resize and adjust one image, from the Claid quick start. Use your own API key and image URL.
```bash
curl -X POST --location "https://api.claid.ai/v1/image/edit" --http1.1 \
    -H "Host: api.claid.ai" \
    -H "Authorization: Bearer {YOUR_API_KEY}" \
    -H "Content-Type: application/json" \
    -d "{
            \"input\": \"https://claid.ai/doc-samples/bag.jpeg\",
            \"operations\": {
                \"resizing\": {
                    \"width\": 800,
                    \"height\": 800,
                    \"fit\": \"crop\"
                },
                \"adjustments\": {
                    \"hdr\": 60,
                    \"sharpness\": 40
                }
            },
            \"output\": {
                \"format\": {
                    \"type\": \"jpeg\",
                    \"quality\": 90
                }
            }
        }"
```

### 3. Bria

*Best for packshots from models trained on licensed data*

![Bria screenshot](https://assets.wireflow.ai/competitors/bria-ai-2021cd424fac.png?v=r5)

- **What it is:** [Bria](https://bria.ai/) is a visual AI platform for generating and editing images and video, trained on fully licensed data. Its Product Shot Editing endpoints cover cutouts, packshots, shadows and lifestyle shots made from text or from a reference image.
- **Best for:** Brands that care about licensed training data and want product shots from an API, an official SDK or an MCP server.
- **Pricing basis:** It charges per request on pay as you go. Product Cut Out, Product Shadow and Background Removal cost $0.018 an image, and Lifestyle by Text, Lifestyle by Image and Background Generation cost $0.03 an image. There are 100 free generations with no card needed. See the [Bria pricing page](https://bria.ai/pricing), checked October 2026.
- **Standout:** The v2 endpoints are asynchronous by default and return a `request_id` and a `status_url`. Passing `webhook_url` makes Bria POST the result when the job finishes, signed with HMAC-SHA256 and retried with exponential backoff for up to 5 attempts over 45 minutes. Source: [Bria's async requests guide](https://docs.bria.ai/getting-started/async-requests).
- **Limit:** The Free plan is capped at 10 requests a minute and pay as you go at 60, with 1,000 on Enterprise, and a 429 comes back above the limit. The older `/v1/product` endpoints are synchronous by default while the newer `/v2/image/edit/product` endpoints are async, so check the version of each endpoint before you design the queue.
- **API or automation:** Bria lists a Python SDK (`pip install bria-client`), a TypeScript SDK (`npm install @bria-ai/client`), an MCP server and agent skills next to the REST API. The product endpoints are described in [the Product Shot overview](https://docs.bria.ai/product-shot-overview).
- **Sources:** [Bria developer docs index](https://docs.bria.ai/llms.txt), checked 2026-10-11 and 2026-10-21.
- **Links:**
  - [Docs](https://docs.bria.ai/)

Pick Bria over Claid when the question of how the model was trained matters to your legal team, or when your code is Python or TypeScript and you want an official client instead of raw HTTP. Pick Claid when the files already sit in a bucket and one call should cover the folder.

Install the official Python SDK, from the Bria docs index (the TypeScript SDK is npm install @bria-ai/client). Set BRIA_API_TOKEN before you run it, as the Bria quickstart shows.
```bash
pip install bria-client
```

### 4. Photoroom

*Best for catalogues kept in a spreadsheet*

![Photoroom screenshot](https://assets.wireflow.ai/competitors/photoroom-4dfc32ae010a.png?v=r5)

- **What it is:** [Photoroom](https://www.photoroom.com/) is an AI platform that edits product photos for online sellers and enterprises. Next to its app it sells a Remove Background API and an Image Editing API that makes AI backgrounds from a text prompt.
- **Best for:** Sellers whose product image URLs live in a Google Sheet or an Excel file and who want each row processed by API.
- **Pricing basis:** The API charges per image: the Plus price is $0.10 an image on the Image Editing API and the Basic price is $0.02 an image on the Remove Background API, and unused images do not roll over. A sandbox gives 1,000 watermarked calls a month with no card. App plans start at Pro, $7.50 a month billed yearly. See the [Photoroom API pricing page](https://www.photoroom.com/api/pricing), checked October 2026.
- **Standout:** Photoroom's docs include a Google Apps Script for a sheet of image URLs. It calls the API for each row, saves the results to a Google Drive folder, writes Processed or Error into a status column and skips rows already marked Processed. Source: [the Google Sheets tutorial](https://docs.photoroom.com/integrations/how-to-process-images-from-google-sheets).
- **Limit:** The API processes one image per call, with a default rate limit of 60 images a minute and a 429 above it, and higher limits are for Enterprise plans. The docs describe no webhook, no asynchronous job endpoint and no batch endpoint, so the result comes back in the HTTP response.
- **API or automation:** The Remove Background quickstart is one POST to `https://sdk.photoroom.com/v1/segment` with an `x-api-key` header, and the response body is the result image. Photoroom also lists an MCP that works as a custom connector in Claude, as [the Photoroom API page](https://www.photoroom.com/api) shows.
- **Note:** The API sandbox gives 1,000 watermarked calls a month. A sandbox is not listed here as a free tier.
- **Sources:** [Photoroom API FAQ](https://docs.photoroom.com/getting-started/frequently-asked-questions), [Photoroom pricing](https://www.photoroom.com/pricing) and [the Remove Background quickstart](https://docs.photoroom.com/remove-background-api-basic-plan/quickstart-guide), checked 2026-10-11 and 2026-10-21.
- **Links:**
  - [Docs](https://docs.photoroom.com/)

Pick Photoroom over Bria when your catalogue already lives in a sheet and you want the vendor's own script to work through it, and when a watermarked sandbox is enough to prove the look first. Our own guide to [generating product images for an online store](https://www.wireflow.ai/blog/how-to-generate-ai-product-images-for-your-online-store) walks through the same job on a canvas.

Remove the background from one image, from the Photoroom Remove Background API quickstart. Use your own API key.
```bash
curl --request POST \
  --url https://sdk.photoroom.com/v1/segment \
  --header 'x-api-key: YOUR_API_KEY' \
  --form image_file=@/path/to/your/image.jpg \
  --output photoroom-result.png
```

### 5. Pixelcut

*Best for single edits from code or an agent*

![Pixelcut screenshot](https://assets.wireflow.ai/competitors/pixelcut-275211e78ae5.png?v=r5)

- **What it is:** [Pixelcut](https://www.pixelcut.ai/) is an AI photo and image editing service on web, iOS and Android with background removal, upscaling and generative fill. It also sells a developer API and runs an MCP server for agents.
- **Best for:** Sellers and small teams that clean up product photos at volume and want one simple API call per edit.
- **Pricing basis:** API credits cost $0.01 each in monthly packs from 1,000 credits ($10), and only successful operations use credits. Background Removal costs 5 credits and Generate Background costs 10. The app's Pro plan is $10 a month, or $8 a month billed yearly, with 1,000 batch exports a month. See the [Pixelcut API page](https://www.pixelcut.ai/api), checked October 2026.
- **Standout:** The API has Background Removal, Image Upscaler, Generate Background, Outpaint and Try-On endpoints. The MCP server's `edit_image` tool accepts a single image or an array for parallel processing. Source: [the Pixelcut MCP docs](https://www.pixelcut.ai/docs/agents/mcp).
- **Limit:** The REST API reference lists single operations only, and Pipelines, the saved multi-step workflows, run from an MCP client and not from the REST API. The OpenAPI spec names no webhook, and Generate Background answers with the result in the response. The common rate limit is 5 requests a second per account.
- **API or automation:** The quickstart is one POST to `https://api.developer.pixelcut.ai/v1/remove-background` with an `X-API-Key` header and an image URL, which returns a `result_url`. Result files are deleted after at most 24 hours, so you download and store them yourself, as [the Pixelcut quickstart](https://www.pixelcut.ai/docs/developer-guide/getting-started/quickstart) says.
- **Note:** The Free plan is the app plan with limited background removal and upscaling. API credits are bought separately.
- **Sources:** [Pixelcut pricing](https://www.pixelcut.ai/pricing) and [the Pixelcut docs home](https://www.pixelcut.ai/docs), checked 2026-10-11 and 2026-10-21.

Pick Pixelcut over Photoroom when an agent should run a saved multi-step Pipeline through MCP, because Photoroom's API docs describe single calls only. Pick Photoroom when you want the spreadsheet script ready-made.

Remove the background from one image, from the Pixelcut API quickstart. The response carries a result_url that is deleted after at most 24 hours.
```bash
curl -sS "https://api.developer.pixelcut.ai/v1/remove-background" \
  -H "X-API-Key: <YOUR_API_KEY>" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -d '{
    "image_url": "https://cdn3.pixelcut.app/product.jpg"
  }'
```
Or add the Pixelcut MCP server to Claude Code, from the Pixelcut MCP docs.
```bash
claude mcp add pixelcut --transport http https://mcp.pixelcut.ai/mcp
```

### 6. Flair

*Best for branded scenes arranged by a designer*

![Flair screenshot](https://assets.wireflow.ai/competitors/flair-0686b6a2961a.png?v=r5)

- **What it is:** [Flair](https://flair.ai/) is an AI product photo generator and editor for ecommerce images. Its homepage describes a drag and drop canvas, reusable templates, real-time team collaboration and custom models trained on your products.
- **Best for:** Ecommerce sellers who need branded product photos and have a person who will arrange each scene.
- **Pricing basis:** Monthly plans: Free at $0 with 1 custom model, 5 generated images and 1 video generation, Pro at $8 a month, Pro+ at $26 a month with 80 generated images, and Scale at $38 a month with 150 generated images. Enterprise is custom. See the [Flair pricing page](https://flair.ai/pricing), checked October 2026.
- **Standout:** You train custom models on your own products and generate images with them, and the Pro+ and Scale plans include a company commercial license.
- **Limit:** API access is listed as early access on Scale and unlimited on Enterprise, and the free plan allows only 5 generated images. The [Flair API page](https://flair.ai/key-features/flair-api) asks you to sign up for access and shows no public endpoint reference.
- **API or automation:** A public API reference is not published. A Bulk Content Generation feature lets you upload product images, pick content types and generate, though no plan on the pricing page names it. Source: [Flair's bulk content generation page](https://flair.ai/key-features/bulk-content-generation).
- **Note:** API access is listed as early access on Scale and unlimited on Enterprise, and no public API reference is published (checked 2026-10-11).
- **Sources:** the Flair homepage, pricing page, API page and bulk generation page linked in this entry, checked 2026-10-11.

Pick Flair over Pixelcut when a designer will compose each scene by hand and a custom model of the product matters more than an API. It sits low on this list only because the criterion is calling a tool from code.

### 7. Pebblely

*Best for quick bulk shots from inside the app*

![Pebblely screenshot](https://assets.wireflow.ai/competitors/pebblely-f03947208f28.png?v=r5)

- **What it is:** [Pebblely](https://pebblely.com/) is an AI tool that makes product photos by placing your product in generated backgrounds. Every plan lists 40+ background themes and custom prompts.
- **Best for:** Small ecommerce sellers who want quick product photos in bulk and are happy to run the batch in the app.
- **Pricing basis:** Monthly plans by image count: Lite at US$9 with 30 images, Basic at US$19 with 200 images and Pro at US$39 with 500 images. The pricing page lists no free plan. See the [Pebblely pricing page](https://pebblely.com/pricing/), checked October 2026.
- **Standout:** When you first save a product, Pebblely extracts its visible text, such as brand names and ingredients, and uses it during generation so the photos keep the correct labels. A group shot arranges up to 5 selected products in one scene. Source: [Pebblely's how-to guide](https://pebblely.com/how-to/).
- **Limit:** Lite does not include bulk generate, and images are capped per month by plan. High-resolution mode costs 2 credits an image instead of 1.
- **API or automation:** The site lists no public API, and no page on it links to API docs. Bulk generation on the Basic and Pro plans runs in the app, as [the Pebblely FAQ](https://pebblely.com/faq/) describes.
- **Note:** The site lists no public API (checked 2026-10-11). Bulk generate runs in the app on the Basic and Pro plans.
- **Sources:** the Pebblely homepage, pricing page, how-to guide and FAQ linked in this entry, checked 2026-10-11.

Pick Pebblely when a person will run the batch by hand and the monthly image count fits, because it is the simplest tool here to start with. Every other entry fits better once the catalogue has to move without someone clicking Generate selected.

## What each check means

A check means the vendor's own source documents it. A cross means the source says it works another way. Anything in brackets is not published, or not verified for this list, which is not proof that it is absent.

- **Public REST API:** A REST API with a public reference that a small team can read before it signs anything.
- **Async job with polling:** A request returns an ID straight away and you poll it, so a slow generation does not hold your connection open.
- **Completion webhook:** The service calls your URL when a job finishes, so a worker does not have to poll.
- **Many images in one request:** One call covers many product images, through a batch endpoint, a folder or a saved batch workflow.
- **Background removal:** Cutting the product out of its background is a documented operation.
- **MCP server:** A documented Model Context Protocol server, so an agent such as Claude can call the tool.
- **Official SDK:** A client library published by the vendor itself.

## How this list is maintained

Every cell comes from the vendor's own docs, pricing page, API reference or FAQ, last checked on 11 October 2026, and the quickstarts were copied from the vendors' docs on 21 October 2026. The numbered order is editorial and uses 4 checks: whether a public API reference exists, whether one call can cover many products, how a finished job reports back, and whether a failed or slow job is easy to detect from code. Tools that leave the least clicking to a person come first. The capability score in the README is a separate plain count of documented checks, and it does not set the order. Nothing here was benchmarked, so no image was generated and no price was tested.

We left out general design apps whose product photo tools run only inside an editor with no batch path, and image model APIs that do not offer product-specific operations, because this list is about catalogue work. To correct a cell, open an issue or a pull request with the tool, the check and a link to the vendor page that proves it. PRs are welcome, including corrections to entry 1.

- [`data/tools.json`](data/tools.json) is the source of truth. The tables in this README are generated from it and are overwritten on every run, so edit the JSON, not the tables.
- [`scripts/update.js`](scripts/update.js) fetches star counts and latest release tags from the GitHub API for the tools that publish an official repo, stamps the check date, and regenerates the tables. `--offline` regenerates without the network; `--check` exits non-zero if the README has drifted from the data.
- [`.github/workflows/refresh.yml`](.github/workflows/refresh.yml) runs it weekly and on manual dispatch, and commits only when the data actually changed.
- Prices are deliberately not stored as numbers. A stale price in a comparison table is worse than no price, so the table links to each vendor's own pricing page.

## FAQ

<details>
<summary><strong>What is the best AI product photography software?</strong></summary>

It depends on how the images will be made. If a script or a worker has to process the catalogue, Wireflow, Claid and Bria document the most from code. If a person will work through the images by hand, Pebblely and Flair are simpler, and Photoroom sits in between with a sheet script.

</details>

<details>
<summary><strong>Can I use AI for product photography?</strong></summary>

Yes. Every tool on this list makes product images with AI, from background removal and new scenes to packshots with shadows. Check the licence terms of each plan before you publish, for example Flair lists a company commercial license on its Pro+ and Scale plans.

</details>

<details>
<summary><strong>Can you automate product photography?</strong></summary>

Yes, with a tool that has an API. Claid has a batch endpoint over a storage folder, Bria and Wireflow send a signed webhook when a job finishes, and Photoroom's docs include a Google Sheets script. On Wireflow a saved workflow can render many rows in one run, as [the batch generation page](https://www.wireflow.ai/features/batch-ai-generation) explains.

</details>

<details>
<summary><strong>Is there free AI product photography?</strong></summary>

Several tools let you try before you pay. Bria gives 100 free generations with no card, Claid's trial gives 50 credits, Photoroom's API sandbox gives 1,000 watermarked calls a month and Flair's free plan allows 5 generated images. Wireflow's free plan lets you build workflows, and running generations needs a paid plan.

</details>

<details>
<summary><strong>What are the best AI tools for ecommerce product images?</strong></summary>

For catalogue work by API, the first five entries here: Wireflow, Claid, Bria, Photoroom and Pixelcut. Each documents a REST API, and Wireflow, Claid and Bria also document a completion webhook. For a small shop that works in an app, Pebblely and Flair are quicker to learn.

</details>

<details>
<summary><strong>Is there a Claude Code skill for making AI product photos on a white background?</strong></summary>

Yes. Wireflow publishes an open source product photography skill for Claude Code under the MIT license, and it shows the credit cost and waits for your yes before it runs. Pixelcut, Photoroom and Bria also document MCP servers that an agent can call.

</details>

## The short version

Pick Wireflow when one finished product image needs several models in a row and you want to start the chain and receive the result from your own code. Pick Claid when the job is one edit across a folder of files in cloud storage, and Bria when licensed training data and an official SDK matter most. Before you commit, run the same 20 products through your two finalists and note what a failed image costs you in each. To connect an agent to Wireflow first, the setup steps are on [the Wireflow MCP page](https://www.wireflow.ai/mcp).

## Contributing

Corrections and additions are welcome, including corrections to the entry for the tool that maintains this list. Open an issue with the tool name, a working link, one line on what it does that the tools already listed do not, and one line on where it stops. Entries are judged on whether they are usable today, not on popularity. Full rules in [CONTRIBUTING.md](CONTRIBUTING.md).

## License

[CC0 1.0 Universal](LICENSE), public domain. Take the data, fork the list, no attribution required.

---

Maintained by [a1adams](https://github.com/a1adams).
