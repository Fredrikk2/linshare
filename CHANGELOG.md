<a name="2.2.4"></a>
# [2.2.4](https://github.com/linagora/linshare/compare/2.2.3...2.2.4) (2019-04-29) [Download link](http://download.linshare.org/versions/2.2.4/)

**The 2.2.4 release of LinShare is out**

## LinShare components

* **core** : 2.2.5 [changelog](https://github.com/linagora/linshare-core/compare/2.2.3...2.2.5)
* **ui-admin** : 3.2.2 [changelog](https://github.com/linagora/linshare-ui-admin/compare/v3.2.1...v3.2.2)
* **ui-user** : 2.2.3 [changelog](https://github.com/linagora/linshare-ui-user/compare/v2.2.2...v2.2.3)
* **thumbnail-server** : 2.0.3
* **linshare-plugin-thunderbird** : 1.8.0

> **NB :**
You can find the upgrade documentation [here](documentation/EN/upgrade).

### Minor features and fixes
* Core
  * Fix bug related to delete expired shares.
  * Fix MailAttachement injection: if its identifier is not found in the mail content it won't be injected.
  * Fix upgrade task UPGRADE_2_2_MIGRATE_THREAD.
  * Replace Antisamy library by new library to sanitize html injections in upload share email notification.
  * Private keys are now revealed only in trace mode.
  * Add full flat mode flag to WorkGroupNodeRestServiceImpl.
  * Add AOP for transaction for safe facade.
  * Fix create permission for safe role in workgroup node RAC.
  * Use safeDocumentFacade for uploading file with Safe role.
  * Fix upload with RIC (using safe role).
  * Fix Statistic daily batch when user is purged.
  * Fix update domainQuota, default-quota can't be over quota in the same domain.

* UI-User
  * Fix copy rights in workgroups
  * Fix russian translation of relative time (last time file edition)
  * Search filter:
      * New property added authorNameTranslated for audit items
      * This property is now used to filter the table on search
      * Use the event translateChangeSuccess to trigger translation
  * Fix the translation of audit list on change language
  * Fix audit information : Avoid access to treePath on non-existing property
  * Use angular translate in filter box
  * Add browse template Vitnameese translation and some other keys
  * Enforce email format when setting a contactList contact
  * Fix bug of deleting selected workgroups
  * Fix dropdown for the bottom of the list
  * Prevent copying files to personal space for users with wrong rights
  * Add file size audit value in details of creation action
  * Remove ruby-sass and use node-sass
  * Hide create-contact-list-from-workgroup-members when the functionality is disabled
  * Fixes of Autocomplete: Redirect to create a guest if functionality is enabled and improve error's management
  * Fixes : resetPassword:
      * Fix issue with html which was preventing element to be added in the DOM
      * Remove complexity in favor of translate directive
  * Fix the russian translation in the notification pop up
  * Remove MaterialAdmin controller:
      * Use device detector instead for mobile mode
      * Move sidebar toggle logic in UiUserMainController
      * Remove useless complexity of toggleSidebarDirective
  * Fix welcome message translation on language change
  * Add the French translation for the action refresh for the toaster alert
  * Fix long name display in dropdown list
  * Add max file size in the detail of a workgroup
  * Add dependencies between the resolver
  * Remove css property who shift the calendar and dropdown menu
  * Fix build Date locales

* UI-Admin
  * Manage Can create guest for users.
  * Show file size in audit trace when available.
  * Russian Translation for email activation keys.
  * Add the tab for Russian to the tabs managment of Mail layout and Mail footer
  * Fix translation of language selector.
  * MailContent preview: Change layout
  * Russian translation added to welcome message and mail content
  * Upgrade bower to the latest version.

<a name="2.2.3"></a>
# [2.2.3](https://github.com/linagora/linshare/compare/2.2.2...2.2.3) (2019-02-05) [Download link](http://download.linshare.org/versions/2.2.3/)

**The 2.2.3 release of LinShare is out**

## LinShare components

* **core** : 2.2.3 [changelog](https://github.com/linagora/linshare-core/compare/2.2.2...2.2.3)
* **ui-admin** : 3.2.1 [changelog](https://github.com/linagora/linshare-ui-admin/compare/v3.2.0...v3.2.1)
* **ui-user** : 2.2.2 [changelog](https://github.com/linagora/linshare-ui-user/compare/v2.2.1...v2.2.2)
* **thumbnail-server** : 2.0.3
* **linshare-plugin-thunderbird** : 1.8.0

> **NB :**
You can find the upgrade documentation [here](documentation/EN/upgrade).

### Minor features and fixes
* Core
  * Fix importing Roles Writer and Reader on workroups.
  * Fix purge domain
  * Remove thumbnail uuid if file does not exist in datastore during upgrade
  * Fix sql Migration script 2.2
  * Upgrade jackson to 2.9.8
  * Add catch clause when underlying file is missing when computing sha256sum
  * Fix fileDataStore upgrade task
  * Fix duplicate public key
  * Fix update permission for workgroup
  * Add a new check to avoid upgrading LinShare without completing upgrade
  * Update default quota when default quota override is null

* UI-User
  * Bugfix:
      * Date: include formating depending on languages locales
      * Autocomplete: UI - response template of user with only email has been fixed
      * Language:
          * Selector: correct proper loading of language on some case
          * Loading: change way of loading corresponding language
          * VN: correct format file language
  * Feature:
      * Configuration:
          * Add availability to customize behavior of menulink, can now be greyed instead of hidden
          * Add availability to hide the 'Home' menu link
          * Add availability to change default home page
          * Add availability to suffix the menu name
      * File upload: Warn user on application exit if some file are current being uploaded
      * Language: Add Russian version

* UI-Admin
  * Bugfix:
    * Postinstall script
    * Upgrade task: wqrning button on navbar is now shown properly
    * Language: add some missing translations
  * Feature:
    * Saas compiler: switch from ruby-saas to node-saas
    * Language: Add Russian version

<a name="2.2.2"></a>
# [2.2.2](https://github.com/linagora/linshare/compare/2.2.1...2.2.2) (2019-02-04) [Download link](http://download.linshare.org/versions/2.2.2/)

**The 2.2.2 release of LinShare is out***

## LinShare components

* **core** : 2.2.2 [changelog](https://github.com/linagora/linshare-core/compare/2.2.1...2.2.2)
* **ui-admin** : 3.2.0
* **ui-user** : 2.2.1
* **thumbnail-server** : 2.0.3
* **linshare-plugin-thunderbird** : 1.8.0

> **NB :**
You can find the upgrade documentation [here](documentation/EN/upgrade).

### Minor features and fixes
* Core
  * Fix transient bug when uploading document to workgroups
  * Upgrade spring data to Ingalls-SR16 version
  * Get All system workgroup patterns
  * Refactor the method findAll in public Key api
  * Move all LDAP service and business classes to new package
  * Add new endpoint to find workgroupNode without workgroupUuid
  * fix exception statistic serailization

<a name="2.2.1"></a>
# [2.2.1](https://github.com/linagora/linshare/compare/2.2.0...2.2.1) (2018-10-31) [Download link](http://download.linshare.org/versions/2.2.1/)

**The 2.2.1 release of LinShare is out**

## LinShare components

* **core** : 2.2.1 [changelog](https://github.com/linagora/linshare-core/compare/2.2.0...2.2.1)
* **ui-admin** : 3.2.0
* **ui-user** : 2.2.1
* **thumbnail-server** : 2.0.3
* **linshare-plugin-thunderbird** : 1.8.0

> **NB :**
You can find the upgrade documentation [here](documentation/EN/upgrade).

### Fixes
* Core
  * Fix extra field in ldap_pattern inserts.
  * Fix NPE when no readers during LDAP synchro. [#17](https://github.com/linagora/linshare-core/issues/17)
  * Fix NPE accessing ShareEntryGroup
  * Fix anonymous sharing. [#16](https://github.com/linagora/linshare-core/issues/16)
  * Fix anonymous URL authentication. [#16](https://github.com/linagora/linshare-core/issues/16)
  * Fix Context initialization failing because of ehcache.
  * Update thumbnail engine to 2.0.3
  * Fix NPE on StatisticWeeklyThreadBatch.
  * Replace posixgroup by groupOfNames.
  * Fix primary key confilct on LDAP pattern.


* Thumbnail-Engine
  * Update pdfbox version to 2.0.12.


* Linshare-plugin-thunderbird
  * Add support of thunderbird 60.

<a name="2.2.1"></a>
# [2.2.0](https://github.com/linagora/linshare/compare/2.1.3...2.2.0) (2018-10-05) [Download link](http://download.linshare.org/versions/2.2.0/)

**The 2.2.0 release of LinShare is out**

## LinShare components

* **core** : 2.2.0 - [changelog](https://github.com/linagora/linshare-core/compare/2.1.3...2.2.0-1)
* **ui-admin** : 3.2.0 - [changelog](https://github.com/linagora/linshare-ui-admin/compare/v3.1.3...v3.2.0)
* **ui-user** : 2.2.0 - [changelog](https://github.com/linagora/linshare-ui-user/compare/v2.1.3...v2.2.0-1)

> **NB :**
You can find the upgrade documentation [here](documentation/EN/upgrade).

### Main features

  * [JWT login support](documentation/EN/configuration/how-to-use-jwt.md) [DOC] : You can now configure a login setup to use JWT as an  authentication method.

  * [LDAP synchronization](documentation/EN/configuration/configure_ldap_synchronization.md) [DOC] : You can create member groups in your LDAP directory and simply synchronize them with LinShare workgroups.
    - ![Configure domain workgroup provider[SCREENSHOT]](http://download.linshare.org/screenshots/2.2.0/B03.Workgroups.Admin.Domain.Provider.png)

  * [LinShare theming](documentation/EN/configuration/setting_the_theme_for_linshare.md) [DOC] : It is now possible to change your LinShare theme as you may see on screenshots below.
    - ![Default LinShare theme[SCREENSHOT]](http://download.linshare.org/screenshots/2.2.0/A01.Theme.Home.Default.png)
    - ![Darkgreen color applied to LinShare theme[SCREENSHOT]](http://download.linshare.org/screenshots/2.2.0/A02.Theme.Home.Green.png)
    - ![Darkgreen theme user interface[SCREENSHOT]](http://download.linshare.org/screenshots/2.2.0/A03.Theme.User.Green.png)

  * [New workgroup role access management](documentation/EN/user/linshare-user.md#4-shared-spaces) [DOC] : We add a new _CONTRIBUTOR_ role and update rights of the _WRITER_ role.
    - ![Workgroup roles list in user interface[SCREENSHOT]](http://download.linshare.org/screenshots/2.2.0/B01.Workgroups.User.Roles.png)
    - ![List workgroup roles in admin interface[SCREENSHOT]](http://download.linshare.org/screenshots/2.2.0/B02.Workgroups.Admin.Roles.png)

  * Deprecated
    * Thread APIs : The Thread and ThreadMembers API are deprecated and will be removed in a future release. Please use SharedSpaceNode and SharedSpaceMember APIs.<br/>
See documentation [linshare-core-documentation-ws-api-userv2.tar.bz2](http://download.linshare.org/components/linshare-core/2.2.0-1/)

All screenshots are available [here](http://download.linshare.org/screenshots/2.2.0/)

### Minor features and fixes

* User:
  * Added COPY label on mobile
  * Changed User interface documentation
  * Fixed contact lists creation from workgroup members
  * Fixed gui bugs when "Personal Space" functionality is disabled
  * Fixed Html display in autocomplete tooltip
  * Fixed logout button not loggint out

* Admin:
  * Fixed redirection on empty parameter in domain update

* Core:
  * Changed MongoDB and Spring data queries display in info log traces
  * Fixed expiry date label display in emails when this functionality is disabled
  * Upgraded to Apache Commons Collections 3.2.2
  * Upgraded to Apache CXF 3.2.4
  * Upgraded to Apache pdfbox 1.8.14
  * Upgraded to Aspectj 1.9.1
  * Upgraded to H2 1.4.196
  * Upgraded to Hibernate 5.0.12
  * Upgraded to Jackrabbit 2.17.3
  * Upgraded to Javax WS RS 2.1
  * Upgraded to JavaMail 1.4.7
  * Upgraded to Jclouds 2.1.0
  * Upgraded to Jjwt 0.9.0
  * Upgraded to JMXTerm 1.0.0
  * Upgraded to LinShare Thumbnail Engine 2.0.2
  * Upgraded to Mozilla Rhino 1.7.10
  * Upgraded to MySQL driver 8.0.11
  * Upgraded to OpenCMIS 1.1.0
  * Upgraded to PostgreSQL Driver 42.2.2
  * Upgraded to quartz-scheduler 2.3.0
  * Upgraded to Slf4j 1.7.25
  * Upgraded to Spring 5.0.7
  * Upgraded to Spring-data Gosling-SR6
  * Upgraded to Spring-security 5.0.6
  * Upgraded to Spring LDAP Core 2.3.2
  * Upgraded to Swagger JAXRS 1.3.13
  * Upgraded to Thymeleaf 3.0.9


<a name="2.1.3"></a>
# [2.1.3](https://github.com/linagora/linshare/compare/2.1.2...2.1.3) (2018-05-28) [Download link](http://download.linshare.org/versions/2.1.3/)

**The 2.1.3 release of LinShare is out**

## LinShare components

* **core** : 2.1.3
* **ui-user** : 2.1.3
* **ui-admin** : 3.1.3

**NB:**

You can find the upgrade documentation [here](documentation/EN/upgrade).

### Fixes

Users:

 * Bug fixing:
   * JS error
   * Change language by route /language/<lang-code>
   * Menu scroll on small device
   * Access to External: anonymous & change password

* Features:
   * External link in menu: configurable via config.js
   * Debug mode switcher: allow a user to activate the mode debug in realtime!

* Other:
   * Moved config.js to a proper folder config

Core:

 * Fix access to upgrade tasks when simple admin (HTTP 403)

Admin:

 * Fix warning displayed for new upgrade tasks.


<a name="2.1.2"></a>
# [2.1.2](https://github.com/linagora/linshare/compare/2.1.1...2.1.2) (2018-05-28) [Download link](http://download.linshare.org/versions/2.1.2/)

**The 2.1.2 release of LinShare is out**

## LinShare components

* **core** : 2.1.2
* **ui-user** : 2.1.2

**NB:**

You can find the upgrade documentation [here](documentation/EN/upgrade).

### Fixes

Users:

 * Bug fixing:
   * JS error
   * Remove NEW_ITEM from dropdown menu, legacy design
   * Update message on file sharing to use plurality
   * Higlight button on hover
   * Confusing Typo:
   * When adding member: 'search people' to 'add people'
   * When looking at the list of member: 'add people' to 'search people'
   * Handle contact list name error => reset name on error
   * Error message on adding existing member in a workgroup

* Features:
   * Browse component: Add message when no workgroup exists
   * Organize dropdown accross the application to be coherent between themselves and also wih the side menu
   * Display version on two distinctives lines
   * Hide preview button on deactivation of engine
   * Click on thumbnail to open preview
   * Show confirm popup on workgroup member deletion
   * Icon Initial: when member has no information, use email address to fill
   * Replace info and delete icon
   * Duplication of contact list

Core:

 * Amazon AWS-S3 support added.
 * Fix language on **mailContext
 * Thumbnail generator is now disabled by default
 * BugFix NPE when searching users from deleted domains


<a name="2.1.1"></a>
# [2.1.1](https://github.com/linagora/linshare/compare/2.1.0...2.1.1) (2018-05-28) [Download link](http://download.linshare.org/versions/2.1.1/)

**The 2.1.1 release of LinShare is out**

## LinShare components

* **core** : 2.1.1
* **ui-admin** : 3.1.1
* **ui-user** : 2.1.1
* **thumbnail-server** : 2.0.2

**NB:**

You can find the upgrade documentation [here](documentation/EN/upgrade).

### Fixes

Users:

 * Bugfix master hide contactslists in autocomplete
 * Fix copyright on reset password page.
 * Remove useless images
 * bugfix hide receivedshare in home
 * fix typo on anonymous page

Admin:

 * Delete button hidden in Manage domains
 * Traduction for functionalities

Core:

 * Throw error 403 Forbidden when deleting the default welcome message
 * Remove useless properties in linshare.properties.sample
 * Cancel checking role in DelegationGenericFacade
 * JWT : Backport PEM key support for JWT
 * find all domains with purgeStep is IN_USE
 * Updating default path for jwt extra public key
 * Add uuid as optionnal pathParam, to the welcomeMessages update endpoint
 * Add logger to trace which public and private keys were loaded.
 * Fix wrong error code for add member method in workgroups.
 * Fix tests for guest service (quota)
 * fix bug about upload files for the guests
 * Mail notification : fix share url for recipients
 * Improve JWT tests.
 * Fix default RSA resolver.
 * Fix SQL schema version for 2.1
 * Remove query params in fileName when uploading file from URL
 * Add support of Private/Public Key for JWT.
 * SharedKey for JWT was removed.
 * Fix issue related to autocomplete of contact list in workgroup
 * Do not call remote thumbnail server is disabled.
 * Add JWT filter to default security springContext
 * Add checks on required fields for JWT token (iat, sub, exp)
 * Allow only Internal users to generate JWT token
 * Add Issuer for generated JWT token.
 * Handle domain uuid in JWT token
 * Add ldap support for JwtAuthenticationProvider
 * Cleaning JwtAuthenticationProvider
 * Add support of JWT authentication (wip)
 * First step to JWT support (token generation only)
 * rewamping BatchMonthlyTest
 * Unprotect logout endpoints.
 * update mail template in the migration script-2_1
 * FIX #123 thymeleaf template html5 warning
 * Improve download. (using StreamingOutput)
 * Feature #117 Upload of document from URL in delegation context
 * fix global link in multiple fileshares notification
 * Feature #117 : Asynchronous upload from URL in Shared Space
 * Feature #121 : Strict mode for Asynchronous upload of LinShare document in shared space
 * FIX #122 disable warning for hibernate metaadata createLob

Thumbnail:

 * improve quality of large previews
 * fix tempfiles cleaning


<a name="2.1.0"></a>
# [2.1.0](https://github.com/linagora/linshare/compare/2.0.4...2.1.0) (2018-01-31) [Download link](http://download.linshare.org/versions/2.1.0/)

**The 2.1 release of LinShare is out**

## LinShare components

* **core** : 2.1.0-1
* **ui-admin** : 3.1.0
* **ui-user** : 2.1.0-1
* **thumbnail-server : 2.0.1**

**NB:**

You can find the upgrade documentation [here](documentation/EN/upgrade).

### Main features

* [New preview](http://download.linshare.org/screenshots/linshare-ui-user/2.1.0/)
Upload and share big files in your own personal space.

* [Improving Performance](https://youtu.be/KH4OpUB5tjI)
A lot of work was done to improve LinShare performances for Edge, Chrome and
Firefox.


All screenshots are available [here](http://download.linshare.org/screenshots/linshare-ui-user/2.1.0/)


<a name="2.0.4"></a>
# [2.0.4](https://github.com/linagora/linshare/compare/2.0.3...2.0.4) (2017-12-07) [Download link](http://download.linshare.org/versions/2.0.4/)

**The new release of LinShare 2.0.4 is available**

Users:

    Fixes #239: disable rename/remove for nonAdmin in sharedSpace and in nodeWorkgroup
    Fix! Hide menu administrations if all of its sublink are disable
    Bugfix hide guest menu if disable
    Fix! Remove Setting menu in production mode
    Fix! Hide properly guest depending on Functionalities
    Fix! Remove href on logout button

Core:

    Fix notification URL for external sharing.
    support of openstack-swift for jcloud in LinShare added.
    Add new property key to disable trusted ip list for sso.


## LinShare components

* **core** : 2.0.4 - [changelog](https://github.com/linagora/linshare-core/compare/2.0.3...2.0.4)
* **ui-admin** : 3.0.4 - [changelog](https://github.com/linagora/linshare-ui-admin/compare/v3.0.3...v3.0.4)
* **ui-user** : 2.0.4 - [changelog](https://github.com/linagora/linshare-ui-user/compare/v2.0.3...v2.0.4)

## Database updates :

You can load the following SQL script to fix [quotas](https://github.com/linagora/linshare-core/blob/2.0.3/src/main/resources/sql/postgresql/Patch_2.0.3.sql)


<a name="2.0.3"></a>
# [2.0.3](https://github.com/linagora/linshare/compare/2.0.2...2.0.3) (2017-10-05) [Download link](http://download.linshare.org/versions/2.0.3/)

**The new release of LinShare 2.0.3 is available**

Users:

    * Feature : copy between all LinShare storage area
     * copy from received shares to personal space
     * copy from received shares to workgroups
     * copy from personal space to workgroups
     * copy from workgroups to workgroups
     * copy from workgroups to personal space
    * Fixed thumbnails generation.
    * Fixed wrong calculus in quotas (*critical*), cf SQL script Patch_2.0.3.sql
    * And a lot of bug fixes, see component's changelog for more details.
[Video of the new copy feature] (http://download.linshare.org/videos/product/LinShare-2.0.3-demo-new-copy-feature.mpeg)

Administration:

    * Quota graphs and business rules check improved
    * See component's changelog for more details.

## LinShare components

* **core** : 2.0.3 - [changelog](https://github.com/linagora/linshare-core/compare/2.0.2...2.0.3)
* **ui-admin** : 3.0.3 - [changelog](https://github.com/linagora/linshare-ui-admin/compare/v3.0.2...v3.0.3)
* **ui-user** : 2.0.3 - [changelog](https://github.com/linagora/linshare-ui-user/compare/v2.0.2...v2.0.3)

## Database updates :

You can load the following SQL script to fix [quotas](https://github.com/linagora/linshare-core/blob/2.0.3/src/main/resources/sql/postgresql/Patch_2.0.3.sql)


<a name="2.0.2"></a>
# [2.0.2](https://github.com/linagora/linshare/compare/2.0.1...2.0.2) (2017-07-29) [Download link](http://download.linshare.org/versions/2.0.2/)

**The new release of LinShare 2.0.2 is available**

Users:

    * Multiple downloads feature added.
    * Cancel share action added
    * Contextual integration of audit in contactsList and received shares was added
    * Versions of LinShare in left sidebar fixed
    * Suppport of login with something other than an email.
    * And a lot of bug fixes, see component's changelog for more details.

Administration:

    * New Audit V2 added
    * Details quota view improved
    * Quota graph quota for users account added.
    * And a lot of bug fixes, see component's changelog for more details.

## LinShare components

* **core** : 2.0.2 - [changelog](https://github.com/linagora/linshare-core/compare/2.0.1...2.0.2)
* **ui-admin** : 3.0.2 - [changelog](https://github.com/linagora/linshare-ui-admin/compare/v3.0.1...v3.0.2)
* **ui-user** : 2.0.2 - [changelog](https://github.com/linagora/linshare-ui-user/compare/v2.0.1...v2.0.2)


<a name="2.0.1"></a>
# [2.0.1](https://github.com/linagora/linshare/compare/2.0.0...2.0.1) (2017-07-04) [Download link](http://download.linshare.org/versions/2.0.1/)

**New release of LinShare : 2.0.1 is available**

## LinShare components

* **core** : 2.0.1-1
* **ui-admin** : 3.0.1
* **ui-user** : 2.0.1


## Changeg log:

* Audit improved
* Workgroups used space are now displayed
* UploadQueue improved
* Drag and Drop of folders added in SharedSpace
* Error pages and maintenance page were added
* Files download method was improved, especially in anonymousUrls
* Browsers compatibility improved
* Performance improvement of the whole application
* Workgroups feature : files copy, folder or files move
* Login error management improved
* External portal for anonymousUrls revamped
* And a lot of bugs fixes :)

## Database updates :

You can load the following SQL script to fix spelling mistakes in all [email templates](https://github.com/linagora/linshare-core/blob/2.0.1-1/src/main/resources/sql/postgresql/reset-default-emails-config.sql)


<a name="2.0.0"></a>
# [2.0.0](https://github.com/linagora/linshare/compare/2.0.0-beta3...2.0.0) (2017-05-09) [Download link](http://download.linshare.org/versions/2.0.0/)

**The first release of LinShare 2.0 is out**

![Home page](http://download.linshare.org/screenshots/linshare-ui-user/2.0.0/01.MyFiles.fullscreen.png)

## LinShare components

* **core** : 2.0.0
* **ui-admin** : 3.0.0
* **ui-user** : 2.0.0

**NB:**

You must reinstall LinShare to use this version. There is no upgrade support
for older beta versions. Upgrade process for LinShare version 1.12 will come soon.

First of all, you must drop all mongodb collections and postgres
databases, then you have to follow the [initialization procedure of the
installation guide](documentation/EN/installation/linshare-install.md).

### Main features

* [Personal file sharing](http://download.linshare.org/screenshots/linshare-ui-user/2.0.0/03.MyFiles.details.png)
Upload and share big files in your own personal space.

* [Guests](http://download.linshare.org/screenshots/linshare-ui-user/2.0.0/08.Guests.png)
Create guests accounts to provide a LinShare account for your external contacts.

* [Contacts Lists](http://download.linshare.org/screenshots/linshare-ui-user/2.0.0/09.MyLists.png)
Create contact lists to share easily your files with your usual coworkers.

* [Upload queue](http://download.linshare.org/screenshots/linshare-ui-user/2.0.0/00.UploadQueue.png)
Manage your big file uploads within the upload queue, and share them asynchronously.

* [Shared Space](http://download.linshare.org/screenshots/linshare-ui-user/2.0.0/07.ShareSpace.png)
A collaborative place to share files between all members of your organisation.

* [Activity logs](http://download.linshare.org/screenshots/linshare-ui-user/2.0.0/10.Activity.logs.png)
A fully detailed view of all your activity.


All screenshots are available [here](http://download.linshare.org/screenshots/linshare-ui-user/2.0.0/)


<a name="2.0.0-beta3"></a>
# [2.0.0-beta3](https://github.com/linagora/linshare/compare/2.0.0-beta2...2.0.0-beta3) (2016-12-22) [Download link](http://download.linshare.org/versions/2.0.0-beta3/)

## Upgraded components

* **core** : 2.0.0-beta3
* **ui-admin** : 3.0.0-beta3
* **ui-user** : 2.0.0-beta3
* **plugin-thunderbird** : 1.7.1

NB: **You must reinstall LinShare to use this version. There is no upgrade support
form older versions. You must to drop all mongodb collections and postgres
databases, then you have to follow the initialization procedure of the
installation guide.**

### Features

* Guests
* Contacts Lists
* Upload queue

### Screenshots :

![Login page](http://download.linshare.org/screenshots/linshare-ui-user/2.0.0-beta3/login.png)
![Home page](http://download.linshare.org/screenshots/linshare-ui-user/2.0.0-beta3/homepage.png)

[other screenshots](http://download.linshare.org/screenshots/linshare-ui-user/2.0.0-beta3/)


<a name="2.0.0-beta2"></a>
# [2.0.0-beta2](https://github.com/linagora/linshare/compare/2.0.0-beta1...2.0.0-beta2) (2016-10-04) [Download link](http://download.linshare.org/versions/2.0.0-beta2/)

## Upgraded components

* **core** : 2.0.0-beta2
* **ui-user** : 2.0.0-beta2

NB: **You must reinstall LinShare to use this version. There is no upgrade support
form older versions. You must to drop all mongodb collections and postgres
databases, then you have to follow the initialization procedure of the
installation guide.**

### Features

* Shared space (aka groups in LinShare v1)

This is the first beta of LinShare 2.0, it is a new design, fresh look and new
technologies. Try it !

<a name="2.0.0-beta1"></a>
# [2.0.0-beta1](https://github.com/linagora/linshare/compare/1.12.4...2.0.0-beta1) (2016-09-08) [Download link](http://download.linshare.org/versions/2.0.0-beta1/)

## Upgraded components

* **core** : 2.0.0-beta1
* **ui-admin** : 3.0.0-beta1
* **ui-user** : 2.0.0-beta1

### Features

This is the first beta of LinShare 2.0, it is a new design, fresh look and new
technologies. Try it !


<a name="1.12.6"></a>
# [1.12.6](https://github.com/linagora/linshare/compare/1.12.5...1.12.6) (2017-07-18) [Download link](http://download.linshare.org/versions/1.12.6/)

## Upgraded components

* **core** : 1.12.8

### Bug Fixes

* **user** Avoid rollback when we delete data related to a invalid email address (shared files)
* **user** Avoid rollback when we delete data related to a invalid email address (upload request)
* **user** Display document's expiration date in user-ui when possible.
* **core** Fix missing activation notification in grouped mode for the second recipient (upload request)
* **core** Fix MySQL upgrade scripts
* **core** New cleaner job: ComputeDocumentExpirationBatch.
* **core** Better logging for FineUploader: filename is included in error messages.
* **core** Better logging when user upload fails because of TSA.
* **core** Bugfix: 2 cron jobs where accidentally disabled.
* **core** Bugfix: fix possible NPE in cleaning batches.  The NPE could occurs when document already vanished.


<a name="1.12.5"></a>
# [1.12.5](https://github.com/linagora/linshare/compare/1.12.4...1.12.5) (2016-04-05) [Download link](http://download.linshare.org/versions/1.12.5/)

## Upgraded components

* **core** : 1.12.6
* **ui-upload-request** : 1.1.2

### Bug Fixes

* **user** Fix quota when copying a shared file.
* **user** Fix bug #1183 Max file size cannot be disabled in Upload request
* **user** Workaround for virus scanner lib overhead.
* **upload-request** Fix route for 404 page.


<a name="1.12.4"></a>
# [1.12.4](https://github.com/linagora/linshare/compare/1.12.3...1.12.4) (2016-12-22) [Download link](http://download.linshare.org/versions/1.12.4/)

## Upgraded components

* **core** : 1.12.4
* **ui-admin** : 2.6.1
* **ui-upload-request** : 1.1.0
* **plugin-thunderbird** : 1.7.1

### Bug Fixes

* **user** Many fixes about access rights checks (read, write) for groups, group members
  and files inside groups.
* **upload-request** Display the recipient firstname and upload request expiry Date
  on uplod request external page.
* **admin** Fix role labels in domain creation form.
* **thunderbird** Fix uploading file feature with recent Tomcat.


<a name="1.12.3"></a>
# [1.12.3](https://github.com/linagora/linshare/compare/1.12.2...1.12.3) (2016-07-20) [Download link](http://download.linshare.org/versions/1.12.3/)

## Upgraded components

* **core** : 1.12.3

### Bug Fixes

* Fix Proxy error on delegation API for documents.
* Adding new audit trace for user which are purged (fully removed) by the
  system.
* Fix 1.11 to 1.12 sql upgrade scripts.
