==============
Validate_email
==============

Validate_email is a package for Python that check if an email is valid, properly formatted and really exists.



INSTALLATION
============

First, you must do::

    pip install validate_email

Extra
------

For check the domain mx and verify email exits you must have the `pyDNS` package installed::

    pip install pyDNS


USAGE
=====

Basic usage::

    from validate_email import validate_email
    is_valid = validate_email('example@example.com')


Checking domain has SMTP Server
-------------------------------

Check if the host has SMTP Server::

    from validate_email import validate_email
    is_valid = validate_email('example@example.com',check_mx=True)


Verify email exists
-------------------

Check if the host has SMTP Server and the email really exists::

    from validate_email import validate_email
    is_valid = validate_email('example@example.com',verify=True)


Don't allow your users to register with disposable emails
---------------------------------------------------------

Checks are performed against this version of the listing:
https://github.com/martenson/disposable-email-domains/tree/4efb0b0ed43022a78abc768c4f28ba7ed7a37772

    from validate_email import validate_email
    is_valid = validate_email("disposable@yopmail.com", allow_disposable=False)
    assert not is_valid


TODOs and BUGS
==============
See: http://github.com/syrusakbary/validate_email/issues