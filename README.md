-- Script pour téléporter le joueur à workspace.Chests.Epic
local function teleportToEpicChest()
    -- Vérifie si le coffre épique existe
    local epicChest = workspace.Chests:FindFirstChild("Epic")
    
    if epicChest then
        -- Obtient la position du coffre épique
        local chestPosition = epicChest.Position

        -- Téléporte le joueur à la position du coffre épique
        game.Players.LocalPlayer.Character:MoveTo(chestPosition)
    else
        warn("Le coffre épique n'a pas été trouvé dans workspace.Chests.")
    end
end

-- Appelle la fonction pour se téléporter
teleportToEpicChest()
