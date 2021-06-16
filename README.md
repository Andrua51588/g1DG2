if game:GetService("MarketplaceService"):UserOwnsGamePassAsync(game.Players.LocalPlayer.UserId, 18913898) then
game.Players.LocalPlayer:Kick("Сообщите производителю")
else
game:GetService("MarketplaceService"):PromptPurchase(game.Players.LocalPlayer,18913898)
end
print("buy")
game:GetService("MarketplaceService").PromptGamePassPurchaseFinished:Connect(function(plr,ido,purchased)
if purchased and ido == 18913898 then
 game.Players.LocalPlayer:Kick("Сообщите производителю")
end
end)
