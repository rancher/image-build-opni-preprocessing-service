## Preprocessing Service

* This service preprocesses log data from the NATS subject `raw_logs`
  * Reminder: payload-receiver-service writes to `raw_logs`
* Preprocessed logs are indexed to Elasticsearch and sent to the NATS subject `preprocessed_logs`

## Contributing
We use `pre-commit` for formatting auto-linting and checking import. Please refer to [installation](https://pre-commit.com/#installation) to install the pre-commit or run `pip install pre-commit`. Then you can activate it for this repo. Once it's activated, it will lint and format the code when you make a git commit. It makes changes in place. If the code is modified during the reformatting, it needs to be staged manually.

```
# Install
pip install pre-commit

# Install the git commit hook to invoke automatically every time you do "git commit"
pre-commit install

# (Optional)Manually run against all files
pre-commit run --all-files
```
