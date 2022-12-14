# BetterWait
BetterWait is geared towards being an alternative to :WaitForChild(). Its main feature is it allows you to wait for a child recursively. This removes the need for those dreadfully long :WaitForChild() chains. Its also using recursion on the backend, which I have an obsession with.

## Usage
The BetterWait module simply returns a function. Its usage is very straight forward. Simply specify a parent and then a child you would like to wait for. It takes some optional parameters such as "timeout" which is a number and functions similar to the timeout parameter in :WaitForChild() and "isRecursive" which is a boolean and functions similar to recursive in :FindFirstChild().

## Examples
```lua
local betterWait = require(game:GetService("ReplicatedStorage"):WaitForChild("BetterWait"))

-- This will wait for a child that is a direct child of Workspace.
local someRootPart = betterWait(game:GetService("Workspace"), "somePart")

-- This will wait for a child that is anywhere inside of Workspace using a deep search.
-- The 3rd and 4th arguments are the optional ones I mentioned above; Timeout and isRecursive.
local someDeepPart = betterWait(game:GetService("Workspace"), "someDeepPart", 15, true)
```

## Install
### Roblox Workflow
You can get Reco off the Roblox Marketplace here.
https://www.roblox.com/library/11821587520/BetterWait

### Rojo Workflow
Get the `.rbxm` file from the releases page. This file can be used to sync to Studio when using Rojo.

### Raw Files
You can find both the `.lua` and the `.rbxm` files here in the releases section.
