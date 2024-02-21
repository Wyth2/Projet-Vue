<!-- src/components/EmailDetail.vue -->
<template>
    <div>
      <h2>Détails de l'e-mail</h2>
      <div>
        <strong>Sujet:</strong> {{ email.subject }}
      </div>
      <div>
        <strong>Expéditeur:</strong> {{ email.sender }}
      </div>
      <!-- Ajoutez plus de détails ici si nécessaire -->
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        email: {},
      };
    },
    created() {
      // Récupérer les détails de l'e-mail depuis la liste statique
      const emailId = this.$route.params.id;
      this.email = this.emails.find((email) => email.id == emailId);
    },
  };
  </script>
  
  <style scoped>
  /* Ajoutez des styles spécifiques au composant ici */
  </style>
  