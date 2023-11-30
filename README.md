# dev_sasRH8
SAS Deployment ON RHEL 8.x

#### Passing UID/PWD via Variable Reference
```
# Create a secure/hidden file (i.e pwd.sas)
# Contents
%let userid=testuser;
%let pwd=testpwd;

# In another file, reference userid/pwd
%include '~/pwd.sas';
libname testDB odbc database=AB user="&userid."
using="&pwd.";

```
