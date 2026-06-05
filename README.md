# Shop Cloudfall SMP

Welcome to the Cloudfall SMP Shop Configuration repository! 
Here you can contribute to our server's shop by submitting Pull Requests (PRs) with new items or balanced price changes.

## How to Contribute
If you'd like to add a new item to the shop, please edit the appropriate `.yml` file (e.g., `blocks.yml`, `drops.yml`, `miscellaneous.yml`) and follow the format below.

### Item Format

```yaml
    [Next ID Number]:
      type: item
      item:
        material: [MATERIAL_NAME] # Must be a valid Spigot/Paper Material name (e.g., CHERRY_LOG)
        quantity: [Amount] # How many items the player buys/sells at once
      buyPrice: [Price] # Price to buy from the shop
      sellPrice: [Price] # Price to sell to the shop (-1 if not sellable)
      slot: [Slot Number] # GUI Slot number (0-53)
      page: [Page Number] # Optional: If the shop needs multiple pages, specify the page number here
```

### Example
```yaml
    12:
      type: item
      item:
        material: EXPERIENCE_BOTTLE
        quantity: 64
      buyPrice: 5000
      sellPrice: 500
      slot: 24
```

### Important Rules
1. **Material Names**: Ensure you are using the correct uppercase material names. For example, use `EXPERIENCE_BOTTLE` instead of `Bottle o' Enchanting`.
2. **Slots**: Make sure the `slot` you choose isn't already taken by another item on the same `page`.
3. **Prices**: Keep the economy balanced! Ridiculous prices will be rejected.
4. **ID Numbers**: Ensure the `[Next ID Number]` increments correctly from the last item in the list.

Once you have added your item, commit the changes and open a Pull Request. We will review it and merge it if everything looks good!
