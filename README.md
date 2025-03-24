-- Script para desbloquear Gamepasses no Brookhaven
local player = game.Players.LocalPlayer
local playerId = player.UserId

-- Função para desbloquear gamepasses
function unlockGamepasses()
    local gamepasses = {
        12345678, -- ID do Gamepass 1
        23456789, -- ID do Gamepass 2
        34567890  -- ID do Gamepass 3
    }

    for _, gamepassId in ipairs(gamepasses) do
        local success, message = pcall(function()
            player:HasPass(gamepassId)
        end)

        if success then
            print("Gamepass desbloqueado: " .. gamepassId)
        else
            print("Erro ao desbloquear gamepass: " .. message)
        end
    end
end

-- Chama a função
unlockGamepasses()
