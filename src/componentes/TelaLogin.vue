<!-- SCRIPT -->
<script setup>

    // Funções

    function validateFields() {
        const usernameValid = isUsernameValid();
        document.getElementById('recuperar-senha').disabled = !usernameValid;

        const passwordValid = isPasswordValid();
        document.getElementById('botao-login').disabled = !usernameValid || !passwordValid;
    }

    function isUsernameValid() {
        const usuario = document.getElementById("usuario").value;
        if (!usuario) {
            return false;
        }
        return validateUsuario(usuario);
    }

    function isPasswordValid() {
        const senha = document.getElementById('senha').value;
        if (!senha) {
            return false;
        }
        return true;
    }

    function validateUsuario(usuario) {
        return /\S+@\S+\.\S+/.teste(usuario);
    }

</script>

<!-- HTML -->
<template>
    <body>
        <div class="loginPrincipal">
            <div class="cartaoLogin">
                
                <!-- Imagem -->
                <img src="../assets/Lovepik_com-401759033-education-logo.png" alt="Logo" class="logo">
                
                <!-- Campo de texto -->
                <form action="#" method="post" autocomplete="on">
                    <div class="areaTexto">
                        <label for="usuario">Usuário</label>
                        <input type="text" name="usuario" id="usuario" onchange="validateFields()" placeholder="Nome de Usuário" autocomplete="username" required minlength="3" maxlength="30">
                    </div>
                    
                    <div class="areaTexto">
                        <label for="senha">Senha</label>
                        <input type="password" name="senha" id="senha" onchange="validateFields()" placeholder="Senha" required minlength="6" maxlength="20">
                    </div>

                    <!-- Botões -->
                    <div>
                        <button type="button" class="recuperar" id="recuperar-senha" disabled="true">Esqueci a senha</button>
                    </div>
                    
                    <div class="botao">
                        <button type="submit" class="botaoLogin" id="botao-login" disabled="true">ENTRAR</button>
                        <button type="button" class="botaoCadastro">CRIAR CONTA</button>
                    </div>
                </form>
            
            </div>
        </div>
    </body>
</template>