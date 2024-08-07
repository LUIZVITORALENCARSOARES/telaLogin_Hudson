<!-- SCRIPT -->
<script setup>

    let usuario = '';
    let senha = '';

</script>

<!-- HTML -->
<template>
    <body>
        <div class="loginPrincipal">
            <div class="cartaoLogin">
                
                <img src="../assets/Lovepik_com-401759033-education-logo.png" alt="Logo" class="logo">
                
                <form action="" method="post" autocomplete="on">
                    <div class="areaTexto">
                        <label for="usuario">Usuário</label>
                        <input type="text" name="usuario" placeholder="Usuário" autocomplete="username" required minlength="3" maxlength="30">
                    </div>
                    
                    <div class="areaTexto">
                        <label for="senha">Senha</label>
                        <input type="password" name="senha" placeholder="Senha" required minlength="6" maxlength="20">
                        <a href="#">Esqueci a senha</a>
                    </div>
                    
                    <div class="botao">
                        <button type="submit" class="botaoLogin">LOGIN</button>
                        <button class="botaoCadastro">CRIAR CONTA</button>
                    </div>
                </form>
            
            </div>
        </div>
    </body>
</template>