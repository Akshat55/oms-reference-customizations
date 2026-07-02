# Contributing to oms-reference-customizations

Thank you for your interest in contributing to this project! Whether you are an IBM team member, a partner, or a customer — contributions of all kinds are welcome.

## Table of Contents

- [Ways to Contribute](#ways-to-contribute)
- [Before You Start](#before-you-start)
- [Contribution Workflow](#contribution-workflow)
- [Adding a New Example](#adding-a-new-example)
- [Coding Style Guidelines](#coding-style-guidelines)
- [Legal](#legal)
- [Communication](#communication)

---

## Ways to Contribute

- **Add a new customization example** — share a pattern or reference implementation you have built for OMS
- **Improve an existing example** — fix a bug, update it for a newer OMS version, or improve its documentation
- **Report issues** — if an example does not work as described, open an [issue](https://github.com/IBM/oms-reference-customizations/issues/new?template=bug_report.md)
- **Request a new example** — describe a customization scenario you need and open an [issue](https://github.com/IBM/oms-reference-customizations/issues/new?template=example_request.md)
- **Improve documentation** — clearer explanations, better prerequisites, additional context

---

## Before You Start

**For significant new additions**, please [open a discussion](https://github.com/IBM/oms-reference-customizations/discussions) or [raise an issue](https://github.com/IBM/oms-reference-customizations/issues/new?template=example_request.md) first so we can align before you invest significant effort. This avoids situations where a contribution cannot be accepted or requires substantial rework.

For small fixes (typos, broken links, minor corrections), feel free to open a pull request directly.

---

## Contribution Workflow

1. **Fork** the repository on GitHub
2. **Create a topic branch** from `main`:

   ```bash
   git checkout -b my-example-or-fix
   ```

3. **Make your changes** — see [Adding a New Example](#adding-a-new-example) below if you are contributing a new customization
4. **Sign off every commit** (required — see [Legal](#legal)):

   ```bash
   git commit -s -m "Add example: brief description"
   ```

5. **Push** your branch and open a **Pull Request** against `main`
6. A maintainer will review your PR. We aim to respond within a few business days
7. Address any review feedback and update your branch
8. Once approved (LGTM from at least one maintainer), a maintainer will merge your PR

---

## Adding a New Example

Each customization example must be self-contained. When contributing a new example, create a dedicated directory following this structure:

``` bash
<category>/<example-name>/
├── README.md          # Required — see template below
├── <source files>
└── ...
```

Where `<category>` is one of: `backend`, `ui`, `agentic-ai`, `skills`.

### Example README template

Every example must include a `README.md` with at minimum:

```markdown
# <Example Title>

## Overview
Brief description of what this customization does and the problem it solves.

## Prerequisites
- IBM Order Management System version X.x or later (if applicable)
- Any other dependencies or environment requirements

## How to Use
Step-by-step instructions to apply this customization.

## Notes
Any caveats, limitations, or version-specific considerations.

## License
Copyright IBM Corp. 2025 - Present
SPDX-License-Identifier: Apache-2.0
```

### Source file license headers

Every source file must include a license header. The SPDX format is preferred:

``` markdown
#
# Copyright IBM Corp. 2025 - Present
# SPDX-License-Identifier: Apache-2.0
#
```

Adjust the comment syntax to match the file type (e.g., `//` for JavaScript/TypeScript, `<!--  -->` for HTML/XML).

---

## Coding Style Guidelines

- Follow the conventions already established in the category you are contributing to
- Keep examples focused and minimal — demonstrate the pattern, not a full application
- Avoid hardcoded credentials, API keys, or internal IBM URLs
- Use environment variables or placeholder values for any sensitive configuration
- Prefer clarity over cleverness — these examples will be read by people unfamiliar with your codebase

---

## Legal

### Developer Certificate of Origin (DCO)

This project uses the [Developer Certificate of Origin (DCO)](DCO.md) to certify that contributors have the right to submit their contributions under the Apache 2.0 license.

**Every commit must be signed off.** A sign-off is a line at the end of your commit message:

``` git
Signed-off-by: Your Name <your.email@example.com>
```

Add it automatically with:

```bash
git commit -s
```

If you forget to sign off, you can amend the last commit:

```bash
git commit --amend --signoff
```

Or sign off multiple commits:

```bash
git rebase --signoff HEAD~<number-of-commits>
```

The [DCO bot](https://github.com/probot/dco) will check all commits in a PR. PRs with unsigned commits cannot be merged.

### License headers

All source files must carry the Apache 2.0 SPDX header (see [Adding a New Example](#adding-a-new-example) above).

### AI-generated code

If you use AI tools (Copilot, watsonx Code Assistant, etc.) to help write your contribution, you remain responsible for the correctness, originality, and licensing compliance of the submitted code. Please review AI-generated code carefully and comply with [IBM's AI Code Policy](https://w3.ibm.com/developer/docs/open-source/legal-ai-code-policy) if you are an IBMer.

---

## Communication

- **Questions, ideas, general discussion:** [GitHub Discussions](https://github.com/IBM/oms-reference-customizations/discussions)
- **Bug reports & issues:** [GitHub Issues](https://github.com/IBM/oms-reference-customizations/issues)
- **Security vulnerabilities:** see [SECURITY.md](SECURITY.md) — do **not** open a public issue

For a list of maintainers, see [MAINTAINERS.md](MAINTAINERS.md).
