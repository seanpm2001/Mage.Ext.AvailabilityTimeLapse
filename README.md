# Availability Time Lapse

## What does it do?

Small workaround for a Trusted Shops issue concerning products with high delivery times and a fixed availability time lapse.

The module helps guys and shops out there dealing with seasonal stuff like plants and seeds in order to come up with Truseted Shops' specifications of the shop certification.

Products, depending on seasonal availability, may have problems regarding the Trusted Shops customer protection.

By using this module, you have the possibility to define time-lapses and let your (customers) customers know whether the relevant product are saleable or not.

## How to use?

The module already injects a template file where you can achieve most stuff. But if you are planning to remove the cart button for example, you can even more by implementing the Block Class into other views by doing the following magic:

	<?php $atl_className = Mage::getConfig()->getBlockClassName('sota_atl/view'); ?>
	<?php $atl_block = new $atl_className(); ?>
	<?php if ($atl_block->isApplicable() && !$atl_block->isWithinAvailability()): ?>
		<p>Crazy stuff hapening here…</p>
	<?php endif; ?>
