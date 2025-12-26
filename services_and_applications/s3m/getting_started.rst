.. _getting_started:

***************
Getting Started
***************

Retrieving a token
==================

Access to the resources in the OLCF Facility API are restricted to your project via an access token.
This means that when you generate a token using myOLCF it is always scoped to the project itself, not your user account.
For example, if using the compute resource to submit a job via Slurm it will run under your project ``_auser`` account.


    1. Navigate to: https://my.olcf.ornl.gov

    2. Choose "Open" as your "Account type" and login

        .. image:: /images/s3m/myolcf_open_oidc.png
           :align: center
           :width: 100%
           :alt: myOLCF Login Page

    3. Select your appropriate Project under which the token will be associated.

        .. note::
            If your required project does not have the ability to create tokens please contact us for assistance.

        .. image:: /images/s3m/s3m_project_access.png
            :align: center
            :width: 100%
            :alt: S3M Access Revealed via Project

    4. Navigate to the S3M Access -> New Token page and generate a token with the desired permissions and expirations.

        .. note::
            During initial testing we are still establishing what acceptable token expirations can be offered.
            Feedback is always welcome but please be patient as initial values will be changed.

        .. image:: /images/s3m/s3m_token_create.png
            :align: center
            :width: 100%
            :alt: S3M New Token Creation

    5. Finally copy the token and store it someplace safe.

        .. note::
            Once the screen is closed your token will no longer be accessible.

        .. image:: /images/s3m/s3m_token_copy.png
            :align: center
            :width: 100%
            :alt: S3M Token Copy


Using a token
=============

You can refer to `s3m_examples`_ for usage examples


Managing Tokens
===============