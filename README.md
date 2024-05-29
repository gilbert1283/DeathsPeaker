-- Script para trocar a parte da perna direita no jogo Brookhaven do Roblox
local player = game.Players.LocalPlayer
local legId = 16580488790 -- ID da perna direita que você deseja usar

-- Verifica se o script está sendo injetado apenas no seu personagem
if player.Name == "SeuNomeDeUsuario" then
    local character = player.Character
    if character then
        local rightLeg = character:FindFirstChild("Right Leg")
        if rightLeg then
            rightLeg.MeshId = "rbxassetid://" .. legId
            print("Perna direita alterada com sucesso!")
        else
            print("Seu personagem não tem uma perna direita.")
        end
    else
        print("Seu personagem não está carregado.")
    end
else
    print("Este script só funciona para o seu personagem.")
end
