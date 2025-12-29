.. _s3m_examples:

******************
S3M Usage Examples
******************

.. _setup:

Set Up to Use Examples
======================

In order to use the following examples, you will need to do one of the following

Start by setting up your API token for use

.. code-block:: bash

    export S3M_TOKEN=<your-token-here>

TODO: create shell/curl only section

Install the dependencies

.. code-block:: bash

    pip install requests

Create a script with your necessary imports

.. code-block:: python

    import os
    import requests


.. _instrospection_api:

Using the Introspection API
===========================

If there is a need to programmatically check the validity and available usage of a token, the introspection API provides answers:

.. code-block:: bash

    curl -s -H "Authorization: $TOKEN" \
    https://s3m.olcf.ornl.gov/olcf/v1/token/ctls/introspect | jq

    {
      "token": {
        "username": "stf040-api_auser",
        "project": "STF040-api",
        "scopes": [
          "compute-ace",
          "data-streaming"
        ],
        "plannedExpiration": "2024-11-08T14:45:38.756330Z",
        "securityEnclave": "open",
        "description": "docs-example-01",
        "oneTimeToken": false,
        "delayedStart": false,
        "delayDuration": ""
      }
    }


.. code-block:: python

    import os
    import requests

    S3M_BASE_PATH = "https://s3m.olcf.ornl.gov/olcf/v1"
    S3M_TOKEN = os.getenv("S3M_TOKEN")

    headers = {
        "Authorization": S3M_TOKEN,
    }

    introspect_response = requests.get(S3M_BASE_PATH + "/token/ctls/introspect", headers=headers)

    if introspect_response.ok:
        token_spec = introspect_response.json()
        print(token_spec)

    {'token': {'username': 'stf007_auser', 'project': 'STF007', 'permissions': ['compute-ace-ro'], 'plannedExpiration': '2026-01-05T23:01:25.216727Z', 'securityEnclave': 'open', 'description': 'docs-example', 'oneTimeToken': False, 'delayedStart': False, 'delayDate': None, 'ownerName': '<user>', 'grpcPermissions': []}}


.. _slurm_api:

Using the Slurm API
===================

stub

.. _streaming_api:

Using the Streaming API
=======================

stub