# Updates of RHEL / CentOS packages #

This repository contains updates for RHEL / CentOS packages. Currently available is:

* a forward-port of the original postfix-2.3 package to postfix-2.10 for *RHEL 5 / CentOS 5*
  (a port for RHEL 6 / CentOS 6 is available from <http://mstevens.fedorapeople.org/el6/postfix/2.10/>).
  This is done as a naïve update: the original SPEC-file is adopted for the new version as required and relevant patches are taken from the above el6 package. It is not a full backport of the (considerably different) above el6 package.

## Known bugs ##

* If selinux is enabled, *postfix* will trigger an AVC denial when trying to `stat()` `public/pickup`, resulting in delays in the delivery of mail.

