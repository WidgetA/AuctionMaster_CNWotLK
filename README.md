# AuctionMaster_CNWotLK

原插件在 WotLK 的版本支持仅到 3.4.0，个人修复维护以支持 WotLK 的更新，目前仅支持中国大陆服务器的怀旧服。

[原插件地址](https://www.curseforge.com/wow/addons/auctionmaster)

## Change Log
### 2025/3/5
- `src\main\TooltipHook\TooltipHook.lua` 中使用了 `GetContainerItemInfo`, 替换为 `C_Container.GetContainerItemInfo`
- `src\main\Gui\AceGUIWidget-ScrollableSimpleHTML.lua` 中错误调用了`SetFontObject`函数，注释掉了该错误调用
- `src\main\Seller\InventoryHandle.lua` 中使用了 `GetContainerNumSlots` 与 `GetContainerItemInfo`, 替换为 `C_Container.GetContainerNumSlots` 与 `C_Container.GetContainerItemLink`
- `src\main\Seller\Seller.lua` 中使用了 ` GetContainerNumSlots`, `PickupContainerItem`, `GetContainerNumSlots`, 替换为 `C_Container.GetContainerNumSlots`, `C_Container.PickupContainerItem`, `C_Container.GetContainerNumSlots`
- `src\main\Seller\Seller.lua` 中 `SetNormalTexture` 纹理函数会在值为空的时候失效，当值为空的时候替换为正确的 `ClearNormalTexture`
