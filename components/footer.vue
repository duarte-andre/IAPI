<template>
<footer>
    <div class="footer-content">
        <div class="footer-item">
            <p>&copy; 2024 Sua Empresa. Todos os direitos reservados.</p>
        </div>
        <div class="footer-item">
            <a href="#txt-topo">Sobre Nós</a>
        </div>
        <div class="footer-item">
            <a href="#contato">Contato</a>
        </div>
        <div class="footer-item">
            <a href="#privacidade">Política de Privacidade</a>
        </div>
        <div class="footer-item">
            <a href="https://www.facebook.com/iapi.org">Facebook</a>
        </div>
       
    </div>
</footer>

</template>

<style>
footer {
    background-color: #333; /* Cor de fundo do rodapé */
    color: white; /* Cor do texto */
    padding: 10px 0; /* Espaçamento interno (padding) */
    text-align: center; /* Centraliza o texto */
}

.footer-content {
    display: flex; /* Usa flexbox para dispor os itens lado a lado */
    justify-content: center; /* Centraliza os itens horizontalmente */
    flex-wrap: wrap; /* Permite que os itens se movam para a linha seguinte, se necessário */
    gap: 20px; /* Espaçamento entre os itens */
}

.footer-item {
    margin: 0 10px; /* Margem para espaçar os itens do rodapé */
}

.footer-item a {
    color: white; /* Cor dos links */
    text-decoration: none; /* Remove o sublinhado dos links */
    transition: color 0.3s; /* Animação suave na mudança de cor */
}

.footer-item a:hover {
    color: #0eacdb; /* Cor do link ao passar o mouse */
}


</style>