Subdomain Provider DNS Authenticator plugin for Certbot
=======================================================

This certbot plugin is designed to use personal DNS management API. The compatible backend API is available on https://github.com/tugrul/subdomain-provider

Installation
------------

pip3 install certbot certbot-dns-subdomain-provider


Usage
-----

Create a credentials.ini file like following

dns_subdomain_provider_endpoint_url=https://subdomain-api.example.com/subdomain-provider
dns_subdomain_provider_token=aaaaaaaa-bbbb-cccc-dddd-eeeeeeeeeeee

Then execute command like following

certbot certonly --authenticator dns-subdomain-provider --dns-subdomain-provider-credentials ./credentials.ini -d testing123.myauthority.app

Optional parameter
------------------

--dns-subdomain-provider-propagation-seconds 

