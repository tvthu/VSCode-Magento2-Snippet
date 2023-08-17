A nice start to a collection of Magento 2 code snippets for Visual Studio Code!

## Table of Contents

### Logs
<details>
  <summary><a href="#logs">Logs</a></summary>
  <ul>
    <li><a href="#log-with-objectmanager">Log with Object Manager</a></li>
    <li><a href="#log-with-file-content">Log with File content</a></li>
  </ul>
</details>

# Logs

## Log Instructions

### Log With Objectmanager

**Trigger:** `m2.log.objectmanager`

**Output:**
```php
\Magento\Framework\App\ObjectManager::getInstance()->get(\Psr\Log\LoggerInterface::class)->debug(__FILE__ .':' . __LINE__);
\Magento\Framework\App\ObjectManager::getInstance()->get(\Psr\Log\LoggerInterface::class)->debug(json_encode(context));
```


### Log With File content

**Trigger:** `m2.log.putcontent`

**Output:**
```php
file_put_contents('var/log/custom.log', __FILE__ .':' . __LINE__ . PHP_EOL, FILE_APPEND);
file_put_contents('var/log/custom.log', context . PHP_EOL, FILE_APPEND);
```

### Module

**Trigger:** `m2.module.sequence`

**Output:**
```xml
<sequence>
  <module name="Vendor_Module" />
</sequence>
```
