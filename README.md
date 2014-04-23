# Magento HHVM Module Compatibility

## What is this?

This is a standard Magento installation that I use for testing popular module's compatibility with Magento:

  - Modules and their versions are managed through [composer](https://github.com/magento-hackathon/magento-composer-installer).
  - Modules are picked by their popularity, though due to this repository being public there will be no paid extensions. 

## Results

### Working modules

  - AW_Blog
  - Nexcess_Turpentine
  - Cm_Cache_Backend_Redis note:
    - Does not work with named persistent connections. (disable ``persistent``) 
    - Does not work with standalone mode. (disable ``force_standalone``)
  - Made_Cache
  - Aoe_Profiler
  - Danslo_HiphopIndexer
  - Aoe_Scheduler
  - Lesti_Fpc
  - Rubic_FixTotalSorting
  - TBT_EnhancedGrid
  - Phoenix_CashOnDelivery

### Untested modules

  - OnePica_AvaTax


## Please test my module too?

  - Modify composer.json to add your module as a dependency.
  - Ensure that your module cleanly installs and doesn't add any rewrite conflicts.
  - Create a pull request.

## How do you find the time to do this?

[Byte Internet](http://www.byte.nl/) has been nice enough to provide a list of most popular repositories and are sponsoring some of my work on HHVM.
