# foundation-admix
Updated versions of packages that are supplied by the base OS.

1. git

   When doing download get sha256sums.asc file from the base vendor url
   and verify sha256sum signature of the downloaded distro file.

1. asciidoctor

   Need to install ruby and gems before building
   ```bash
   yum install ruby-devel rubygems
   ```
   Before mid-2023 this RPM  was used for the old website only 
   and was installed in /usr/local.

   Current version is needed by git-lfs when making the 
   man pages during the RPM build. No need to install on the cluster

   Contents go to /opt/foundation which is handled by foundation-module.

1. git-lfs

   Version built prior to set-2024 needed specific ruby-gems

   - rubygem-rdiscount
   - rubygem-hpricot
   - rubygem-mustache
   - rubygem-ronn

   As of set-2024 only asciidoctor RPM is needed  duirng the build.
   It provides required asciidoctor gem  and asciidoctor command
   for making man pages.
