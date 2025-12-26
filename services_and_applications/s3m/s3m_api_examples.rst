.. _s3m_examples:

******************
S3M Usage Examples
******************

.. _instrospection_api:

Using the Introspection API
===========================

If there is a need to programmatically check the validity and available usage of a token, the introspection API provides answers:

.. code-block::

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



.. _slurm_api:

Using the Slurm API
===================

stub

.. _streaming_api:

Using the Streaming API
=======================

stub