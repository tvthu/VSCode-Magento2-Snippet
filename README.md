A nice start to a collection of Magento 2 code snippets for Visual Studio Code!

![Visual Studio Marketplace Version](https://img.shields.io/visual-studio-marketplace/v/tvthu.vscode-cm-magento2-snippet)
![Visual Studio Marketplace Installs](https://img.shields.io/visual-studio-marketplace/i/tvthu.vscode-cm-magento2-snippet)
![Visual Studio Marketplace Downloads](https://img.shields.io/visual-studio-marketplace/d/tvthu.vscode-cm-magento2-snippet)
![Visual Studio Marketplace Rating](https://img.shields.io/visual-studio-marketplace/r/tvthu.vscode-cm-magento2-snippet)
![Visual Studio Marketplace Rating (Stars)](https://img.shields.io/visual-studio-marketplace/stars/tvthu.vscode-cm-magento2-snippet)

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
