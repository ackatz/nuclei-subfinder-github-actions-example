# nuclei-subfinder-github-actions-example

> Note: I am not affiliated with Project Discovery or Nuclei in any way and use of this code is at your own risk.

Example repo showing how to run [Nuclei](https://github.com/projectdiscovery/nuclei) scans against your domains/assets with GitHub Actions.

I would recommend using this repository only if you have self-hosted runners (i.e., not billed on minutes). This will cost you money to run if you use GitHub-hosted runners, as the scans may take a relatively long time to run.

## Getting Started

1. Create a template from this repository by [clicking this link](https://github.com/new?template_name=nuclei-subfinder-github-actions-example&template_owner=ackatz) or the "Use this template" button on GitHub.
2. Add your domains to the `domains.txt` file in the root of the repository.
3. Create a GitHub Actions repository secret named `WEBHOOK_URL` with the URL of your webhook receiver (e.g., Slack, Tines, etc.) to receive scan results.
4. Create a GitHub Actions repository variables named: 
   - `NUCLEI_SEVERITIES` (e.g., `critical,high`)
   - `NUCLEI_RATELIMIT` (e.g., `50`)
   - `NUCLEI_TIMEOUT` (e.g., `5`)
   - `NUCLEI_CONCURRENCY` (e.g., `25`)
   - `NUCLEI_RETRIES` (e.g., `2`)
   - `RUNNER_OS` (e.g., `ubuntu-latest`)
5. Go to **Settings** -> **Actions** -> **General** and ✅ check the box next to **Allow GitHub Actions to create and approve pull requests**.

More on [my blog](https://akatz.org/building-my-own-nuclei-scanning-infrastructure/).


