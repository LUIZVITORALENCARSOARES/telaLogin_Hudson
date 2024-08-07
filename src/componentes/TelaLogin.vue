<!-- SCRIPT -->
<script>

    // Funções

    export default {
        data() {
            return {
                usuario: "",
                senha: ""
            }
        },

        computed: {
            isUsernameValid(){
                return this.usuario.length > 3;
            },

            isPasswordValid() {
                return this.senha.length > 6;
            },

            isFormValid() {
                return this.isUsernameValid && this.isPasswordValid;
            }
        },

        methods: {
            validateFields() {
                
            }
        }
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
                        <input type="text" name="usuario" v-model="usuario" @input="validateFields" placeholder="Nome de Usuário" autocomplete="username" required>
                    </div>
                    
                    <div class="areaTexto">
                        <label for="senha">Senha</label>
                        <input type="password" name="senha" v-model="senha" @input="validateFields" placeholder="Senha" required>
                    </div>

                    <!-- Botões -->
                    <div>
                        <button type="button" class="recuperar" id="recuperar-senha":disabled="!isUsernameValid">Recuperar Senha</button>
                    </div>
                    
                    <div class="botao">
                        <button type="submit" class="botaoLogin" id="botao-login":disabled="!isFormValid">ENTRAR</button>
                        <button type="button" class="botaoCadastro">CRIAR CONTA</button>
                    </div>
                </form>
            
            </div>
        </div>
    </body>
</template>