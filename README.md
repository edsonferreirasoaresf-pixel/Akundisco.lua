-- 🔒 Painel Anti-Hit Brainrot (simulação)
-- não altera jogo nenhum, só estética

local ativado = false

function painel()
    print("\n=== Painel Brainrot ===")
    if ativado then
        print("🟢 Modo Anti-Hit: ATIVADO")
        print("✨ Colisão desativada, só o tronco vibra no vazio...")
    else
        print("🔴 Modo Anti-Hit: DESATIVADO")
        print("💀 O brainrot voltou, colisão ON, hits machucam de novo...")
    end
    print("========================")
end

function toggle()
    ativado = not ativado
    painel()
end

-- loopzinho estético
while true do
    io.write("\nPressione [Enter] para alternar painel > ")
    io.read()
    toggle()
end
