# Invisible Spam Protection

## Maintainers

 * Marijn Kampf (Nickname: marijnkampf)
  <marijn at exadium dot com>
   
   http://www.exadium.com/tools/silverstripe/modules/invisible-spam-protection-module/
   
   Sponsored by Exadium Web Development
   
## Introduction

Very simple anti spam protection based on principle that automated spammers enter bogus information in all form fields.

Field is added to form that is hidden using CSS hiding it from human users.

Form is only allowed to be submitted if field is empty.

Includes an EditableInvisibleSpamField to integrate with the UserForms module. 

## Requirements

 * Spam Protection Trunk
 * SilverStripe Trunk

## Install Spam Protection Module

The Spam Protection Module (http://silverstripe.org/spam-protection-module) provides the basic interface for managing the spam protection
so first you need to install that module.

* Add 
```
{
    require: {
	"silverstripe/spamprotection": "1.0.x-dev"
	}
}
```
to your project composer.json 
* or execute the command 
```require "silverstripe/spamprotection": "1.0.x-dev"```
* after both ways you have to execute composer update

## Setting up InvisibleSpamProtection

 * InvisibleSpamProtection should be in your sites root folder.
 * Enable anti spam in mysite/_config.php by adding line
   SpamProtectorManager::set_spam_protector('InvisibleSpamProtector');