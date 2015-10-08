# laravel-magento
Package for accessing a locally installed Magento class within Laravel.

## Usage
Initialize the Mage class after which you can use it the same way you would in the Magento framework.
	Mage::init('admin', 'store');

### Performance
You can init the class with specific modules for better performance.
	Mage::init('admin', 'store', array(), Config::get(laravel-magento.modules));

### Example loading a product by sku
	$product = Mage::getModel('catalog/product')->loadByAttribute('sku', $sku);
