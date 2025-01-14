# Organizations 
Documentation for the Admin view of Shuffle. Best used by administrators.

## Table of contents
* [Introduction](#introduction)
* [Organization Overview](#organization_overview)
* [Cloud Synchronization](#cloud_synchronization)
* [Data collection](#data_collection)
* [Pricing](#pricing)
* [Licensing](#licensing)
* [User Management](#user_management)
* [App Authentication](#app_authentication)
* [Environments](#environments)
* [Schedules](#schedules)
* [Files](#files)
* [Datastore](#datastore)
* [Tenants](#tenants)
* [Statistics](#statistics)
* [Health](#health)
* [Notifications](#notifications)

## Introduction
Organizations are Shuffle's way of organizing data, and can be thought of as tenants. Data from Apps, Workflows, Notifications, Files etc. are all related to an organization from which users gain access based on their access rights. This document is made to explain what the different options for organizations are.

## Organization overview
The organization overview gives access to these things:
* Name Change
* Description Change
* Image change
* Cloud synchronization
* Hybrid Feature overview
* Single Signon options
* Notification Workflows
* Priorities & Notifications
* Licensing (Beta until v1.4.0)
* Statistics (Beta until v1.4.0)
* Branding (Beta until v1.4.0)

This view outlines the basic details of your organizations, which any Admin can change at any time. It can tell you about new updates, features and more that we have in store. The view is slightly different from the cloud version to the on-premises version. Here's how:
* The **cloud** version shows you an API-key. This can be used in the open source version.
* The **open source** version gives you an API-key field. This can be used in the cloud version.
![Organization view](https://github.com/frikky/shuffle-docs/blob/master/assets/admin_example-1.png?raw=true)

### Cloud Synchronization
Cloud synchronization is a FREE feature used to get more capabilities on-premises, that otherwise wouldn't be possible. These range from scalability to collaboration, support, public workflow generation, accessibility and more. The goal is to give access to features that otherwise are impossible to build in a location solution. See [Hybrid Features](#hybrid_features) for more info.

![Cloud sync features](https://github.com/frikky/shuffle-docs/blob/master/assets/admin_example-2.png?raw=true)

#### Setup 
Setting up cloud synchronization requires two things:
1. A user on [https://shuffler.io](https://shuffler.io). Get the API-key.
2. An open source version of Shuffle. [Here's how to set it up](https://github.com/frikky/shuffle/blob/master/install-guide.md)

1. Start by going to [https://shuffler.io/register](https://shuffler.io/register?view=admin) and create an account. 
![Register user](https://github.com/frikky/shuffle-docs/blob/master/assets/admin_example-3.png?raw=true)
2. With an account made, go to [https://shuffler.io/admin](https://shuffler.io/admin). Here you'll find your API-key. Copy it.
![Cloud sync cloud](https://github.com/frikky/shuffle-docs/blob/master/assets/admin_example-4.png?raw=true)
3. Go to your [local instance](http://localhost:3001/admin) at /admin and paste the API-key.
![Cloud sync local](https://github.com/frikky/shuffle-docs/blob/master/assets/admin_example-5.png?raw=true)
4. See the features you get access to.
![Cloud sync local features](https://github.com/frikky/shuffle-docs/blob/master/assets/admin_example-6.png?raw=true)

### Hybrid Features 
Updated November 14th, 2022

Want to try it out? Hybrid Access is Free. 

There are many features that make Shuffle more usable. These are mainly related to accessibility, scalability and collaboration - in that order. For the initial release (v0.8) of Shuffle, we've decided to focus entirely on accessibility. Every feature comes with some of the same basic features, so that you know what you're getting into.

**These basic features are**
* Activation (true or false)
* Limits (none or 0-infinite)
* Privacy & Data sharing (none, minimal, high)
* Type (general, actions, triggers, editor, )
* Description

**These are the categories they fit into**
1. Accessibility - Makes Shuffle easier to use. We make every open source function open source, but some are hard or impossible to make easy for a user to have.
* Collaboration	 - Gives access to shared workflows, apps and general searching. This is to make it possible to learn from each other.
* Scalability 	 - Gives access to use our hardware and servers, e.g. through cloud executions. 

You can see most of our currently planned features on [https://shuffler.io/pricing](https://shuffler.io/pricing).

#### Activation
Activation tells you whether the feature is active. It's indicated by the red or green mark next to the feature on the admin page.
![Cloud sync features indicator](https://github.com/frikky/shuffle-docs/blob/master/assets/admin_example-8.png?raw=true)

#### Limits
Some features have limits. These are features such as SMS and email sending, schedule creation, cloud executions and more. Click each item to learn more.

![Cloud sync features limits](https://github.com/frikky/shuffle-docs/blob/master/assets/admin_example-7.png?raw=true)

#### Description
The description exists to specify what exactly an action does. This will become more granular over time. Access it by clicking each feature.

#### Data collection 
There are three types of data sharing, where the initial launch of Shuffle uses none. You can see the usage as per the image in [limits](#limits)

The three levels we'll keep to are:
* None 	- Shuffle doesn't collect any information about your on-premises organization. This is most features.
* Minimal - Shuffle collects a minimal amount of information necessary to execute the action. An example is a Workflow execution, where we'll need to gather information about the next steps in a workflow to properly execute it.
* High 	- Shuffle collects the necessary information to handle information. This is used for when full synchronization, meaning information used on-premises will also be used in the cloud. An example is having access to edit workflows in the cloud, that will execute on-premises. This requires access to all the same apps, workflows, credentials, triggers, organizational users and more. **PS: This will not happen for a while, and will be 100% OPTIONAL**

### Pricing 
[Our pricing tiers for Shuffle](https://shuffler.io/pricing) are currently split into three: Basic, Community and Pro. Basic is a support tier, and exists to make it possible for you to support us without having to use alternative means such as [github sponsors](https://github.com/sponsors/frikky). Everything we build out that can be priced is for us to further create a better offering for the open source community. 

Whenever we add new features that can help Shuffle work better by leveraging cloud resources, you'll automatically get access to it if you're on that tier.

These are our tiers:
* Free 
* Enterprise / Scale 

#### Free 
The basic tier is meant as a way for people to support Shuffle. It will give more perks over time, but to start of, it gives you and your team an onboarding meeting with Shuffle to get you kickstarted as well as some community support features.

#### Enterprise/Scale 
Pro is the full package. It is meant for those of you who want everything from support to auditlogging, datacenter choices, compliance overviews, data retention control, reporting, and more. This package is currently not available as 

Get in touch at [support@shuffler.io](mailto:support@shuffler.io) if you want something more specific.

## User management
![User management Shuffle](https://github.com/frikky/shuffle-docs/blob/master/assets/admin_example-9.png?raw=true)

User management is all about adding, listing, deleting and controlling users in general. Users are a part of a specific organization, and are created by organization admins. To add users you need the "admin" role.

**Existing roles**:
* Org-Admin - Gives access to control an organization, and see what everyone in the organization are doing.
* Org-User - Gives access to use the organizations resources, but NOT see everyone elses Workflows. This role is meant for engineers who are to build their own workflows, without potentially breaking others'
* Org-Reader - Gives access to READ all data for an organization (like an admin), but not make any changes.

**To come:**
* Creating API-only users (no login)
* Granular access (RBAC)

### Adding a user
Click the "ADD USER" button, and you'll get a popup. Type in their username (open source) or email (cloud), and you'll create an invite for them. Cloud will not allow an admin to set a password to share, but rather send them an email. This will also be a part of the hybrid offering later.

![Adding a user to shuffle](https://github.com/frikky/shuffle-docs/blob/master/assets/admin_example-10.png?raw=true)

### Change a users' role
Click the "Role" dropdown and choose one. Defaults are Admin and User, but we'll add granular access for this now. To repeat, here's the current roles:
* Admin - Gives you access to control an organization, and see what everyone in the organization are doing.
* User  - Gives you access to YOUR resources within an organization. This is to prevent you from seeing what everyone else are doing.

### Deleting a user
A user in Shuffle can't be deleted, but deactivated. This is to keep all references available for when audits eventually require them. Click "Edit user", then "Deactivate". This prevents the user from being used. **A deactivated user can be reactivated.**

## App Authentication
App authentication is a way for Shuffle to keep track of what credentials you have for an app in a specific organization. It shows you information the most important information, and gives you access to modify or easily delete them. Authentication is specified at the app level, and applies to ALL functions of the the app, unless specified otherwise. Authentication is created during workflow editing.

![Basic app authentication](https://github.com/frikky/shuffle-docs/blob/master/assets/admin_example-11.png?raw=true)

These are **NOT** editable outside of deletion as of november 2020, but we may add the possibility of changing without showing the previous value. 

### Authentication Field overview 
The fields of authentication
* Icon 					- The App's icon. This is 
* Label 				- The name of the authentication scheme. Make it helpful, e.g. "QRadar Datacenter Amsterdam" or similar. 
* App Name 			- The name of the app it belongs to
* Workflows 		- The amount of workflows it's being used in
* Action Amount - The amount of actions that use the authentication
* Fields 				- The fields specified by the app creator. It's usually a URL, an API key or username & password.
* Actions 			- What you can do to edit the app. As of 20.11.2020, only deletion is accessible. By deleting it, you'll also make the **workflow invalid**.

### Authentication in workflows 
Authentication is and should be defined the first time you use an app. We'll use the example of TheHive, which takes the fields "apikey" and "url". Start by [creating a workflow](/docs/workflows#create), before dragging in the app "TheHive". 

Once it's in, click the node, and you'll see a view like this. We've outlined three places that indicate this app requires authentication. All of these are also clickable.
![Authentication in workflow](https://github.com/frikky/shuffle-docs/blob/master/assets/admin_example-14.png?raw=true)

By clicking either of these, a popup window will show. In this one, type in a DESCRIPTIVE name (to remember), before passing credentials. **PS: Never use localhost in an URL. Everything runs in a container, which has its own IP. Always use the system's IP/domain within the URL.**
![Authentication workflow popup](https://github.com/frikky/shuffle-docs/blob/master/assets/admin_example-15.png?raw=true)

By clicking "submit", the authentication is now saved for your organization. This removes clutter in the UI, by having less required fields, and is also reusable. You can now make multiple nodes that use the same authentication.
![Authentication view after submit](https://github.com/frikky/shuffle-docs/blob/master/assets/admin_example-16.png?raw=true)

Last, but not least, this can now be controlled on an organizational level. 
![The same authentication on](https://github.com/frikky/shuffle-docs/blob/master/assets/admin_example-17.png?raw=true)

### App creation with authentication
The fields are specified by the app creator. This short section outlines how to create authentication as a creator. [More on this in the apps section](/docs/apps). An example is TheHive, which takes a URL and an API-key. These fields have to be specified as seen below. 
![App creation specification](https://github.com/frikky/shuffle-docs/blob/master/assets/admin_example-12.png?raw=true)

Outer level: authentication
Inner level: parameters

These parameters are specified exactly as a parameter within an action. The function's code needs to reflect it as well, as can be seen with this python function, taking an apikey and URL.
![App creation python code](https://github.com/frikky/shuffle-docs/blob/master/assets/admin_example-13.png?raw=true)

## Environments
Environments are a core part of Shuffle's open source build. Think of it as physical location where you want an agent of Shuffle running (Orborus). Orborus is the tool that keeps your workflow running. But Orborus needs to know what jobs to run. After all, we'd like it you to be able to run parts of a workflow in the cloud and parts of it in all your different datacenters. 

![Environments in Shuffle](https://github.com/frikky/shuffle-docs/blob/master/assets/admin_example-19.png?raw=true)

The default environment is called "Shuffle" in your on-premises environment, and "Cloud" in your cloud environment. You can add as many as you want, but you'll only get access to "cloud" environments through cloud synchronization.  

### Environment fields
* Name 						- The name to use. This is the identifier used by orborus. 
* Orborus running	- Shows whether Orborus is running or not.
* Type 						- Whether it's a cloud environment or not. Orborus can't attach to "cloud" environments.
* Default					- Whether it's the default environment to use for new actions. You should set this to the environment you use the most.
* Actions 				- Possible changes to an environment. Currently only archiving. You can't re-open an archived environment, and can't archive the default environment.
* Archived				- Tells you whether it's archived. There's a toggle at the top to edit it.

### Orborus configuration
If you would like to run Orborus towards a different environment, you'll have to specify the environment variables "ENVIRONMENT_NAME", "ORG", "AUTH" and "BASE_URL". AUTH and ORG may not be required.

Here's an example, where the environment's name is "Hallo" and it's using https://shuffler.io as it's backend. This works on-premises as well.
```
docker run \
	--volume /var/run/docker.sock:/var/run/docker.sock \
	-e ENVIRONMENT_NAME="Another env" \
	-e AUTH="Auth from the environment" \
	-e ORG="Your org ID from the /admin UI top right" \
  -e DOCKER_API_VERSION=1.40 \
	-e BASE_URL=http://192.168.86.51:5002 \
	ghcr.io/frikky/shuffle-orborus:nightly

```

### Health

We now have a health check API that can be used to check the health of your shuffle instance. It's related endpoints are available at:

-  `/api/v1/health`: This gives you the result of the cached execution (doesn't require an API key)
-  `/api/v1/stats`: This gives you historical data about the health of your instance (doesn't require an API key)

You can also force a run by making an API call at:
- `/api/v1/health?force=true` (calling this requires the API key of an admin user)

For the time being, this health check automatically runs every 15 minutes by default. 


### Notifications

Notifications are a way for Shuffle to tell inform you of an error in your workflows. We send you notifications in two ways:
- Through the UI: You'll see a bell icon with a number next to it, on the top right when you're logged in. This indicates the amount of notifications you have. Clicking it will show you the notifications.
- Through workflows: If you go to `https://shuffler.io/admin?admin_tab=organization`, you'll see a section called "Notification Workflow". Click on it to select an appropriate workflow. This workflow will be executed whenever a notification is created. This can be used to automate opening tickets, sending emails, or whatever you want to do when there is an error in your notification.

We use some sort of "bucketing" of notifications, to prevent you from getting spammed. This means, every time a notification is created 2 times under 2 minutes, we'll only send you one notification. This is to prevent you from getting spammed.

If you're on the open-source side, you can change this by changing the `SHUFFLE_NOTIFICATION_BUCKETING_MINUTES` environment variable. This is set to 2 minutes by default.

