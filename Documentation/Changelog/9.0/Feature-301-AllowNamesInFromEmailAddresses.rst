.. include:: ../../Includes.rst.txt

=====================================================
Feature: #301 - Allow names in "from" email addresses
=====================================================

See `Issue 301 <https://github.com/extcode/cart/issues/301>`__

Description
===========

It is now possible to define names which will be used when sending emails.
These names will be shown to the customer and shop owner when receiving mails.
Before only the email address was shown.

Impact
======

Negative effects are not expected. No adding the names will just have the same
result as before.

As with all the other mail settings those in the plugin take precedence.


Migration
=========
See also :ref:`the documentation for email addresses <mail_addresses>`.

.. code-block:: typoscript
   :caption: EXT:sitepackage/Configuration/TypoScript/setup.typoscript

    plugin.tx_cart {
       mail {
           // Used for emails sent to the customer (=buyer)
           buyer {
               fromName = Your Brand name
               // the other settings as shown in the documentation
           }

           // Used for emails sent to the shop owner (=seller)
           seller {
               fromName = Cart TYPO3 System
               // the other settings as shown in the documentation
           }
       }
   }

.. index:: TypoScript, Frontend
