<!-- src/components/EmailList.vue -->
<template>
    <div>
      <h2>Liste des e-mails</h2>
      <ul>
        <li v-for="email in emails" :key="email.id" @click="showEmailDetail(email.id)">
          {{ email.subject }} - {{ email.sender }}
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        emails: [], // Les e-mails seront récupérés depuis le backend
      };
    },
    methods: {
      showEmailDetail(emailId) {
        // Rediriger vers la vue détail de l'e-mail avec l'id correspondant
        this.$router.push({ name: 'emailDetail', params: { id: emailId } });
      },
    },
  };
  </script>
  
  <style scoped>
  /* Ajoutez des styles spécifiques au composant ici */
  </style>
  <!-- src/components/EmailList.vue -->
<template>
    <div>
      <h2>Liste des e-mails</h2>
      <ul>
        <li v-for="email in emails" :key="email.id" @click="showEmailDetail(email.id)">
          {{ email.subject }} - {{ email.sender }}
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        emails: [
          { id: 1, subject: 'Premier e-mail', sender: 'expediteur@example.com' },
          { id: 2, subject: 'Deuxième e-mail', sender: 'expediteur2@example.com' },
          // Ajoutez plus d'e-mails ici
        ],
      };
    },
    methods: {
      showEmailDetail(emailId) {
        this.$router.push({ name: 'emailDetail', params: { id: emailId } });
      },
    },
  };
  </script>
  
  <style scoped>
  /* Ajoutez des styles spécifiques au composant ici */
  </style>
  