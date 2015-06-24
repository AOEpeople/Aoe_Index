Aoe_Index
=========

Improve Index management in Magento. Enables Magento to process indexes asynchronously

What does it do?

1. Adds new mode `async` to index_process
2. Change behaviour of `Mage_Index_Model_Process->reindexAll()` to process the queue Magento stores in `index_event` table instead of reindexing all data. (Only for indexers with mode set to async)
3. Prevents Magento from reindexing product during product save (just queue the event)
