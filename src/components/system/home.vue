<!--
Copyright 2017 ODK Central Developers
See the NOTICE file at the top-level directory of this distribution and at
https://github.com/getodk/central-frontend/blob/master/NOTICE.

This file is part of ODK Central. It is subject to the license terms in
the LICENSE file found in the top-level directory of this distribution and at
https://www.apache.org/licenses/LICENSE-2.0. No part of ODK Central,
including this file, may be copied, modified, propagated, or distributed
except according to the terms contained in the LICENSE file.
-->
<template>
  <div>
    <page-head>
      <template #title>{{ $t('title') }}</template>
      <template #tabs>
        <li :class="tabClass('backups')" role="presentation">
          <router-link :to="tabPath('backups')">
            {{ $t('tab.backups') }}
          </router-link>
        </li>
        <li :class="tabClass('audits')" role="presentation">
          <router-link :to="tabPath('audits')">
            {{ $t('tab.audits') }}
          </router-link>
        </li>
      </template>
    </page-head>
    <page-body>
      <router-view/>
    </page-body>
  </div>
</template>

<script>
import PageBody from '../page/body.vue';
import PageHead from '../page/head.vue';
import tab from '../../mixins/tab';

export default {
  name: 'SystemHome',
  components: { PageBody, PageHead },
  mixins: [tab()],
  computed: {
    tabPathPrefix() {
      return '/system';
    }
  }
};
</script>

<i18n lang="json5">
{
  "en": {
    // This is the title of the page for managing backups, audit logs, and other system-level functions.
    "title": "System Management",
    "tab": {
      "backups": "Backups",
      "audits": "Server Audit Logs"
    }
  }
}
</i18n>

<!-- Autogenerated by destructure.js -->
<i18n>
{
  "cs": {
    "title": "Řízení systému",
    "tab": {
      "backups": "Zálohy",
      "audits": "Protokoly auditu serveru"
    }
  },
  "de": {
    "title": "System-Management",
    "tab": {
      "backups": "Sicherheitskopien",
      "audits": "Server Audit Logs"
    }
  },
  "es": {
    "title": "Administración del sistema",
    "tab": {
      "backups": "Copias de seguridad",
      "audits": "Registro de auditoría"
    }
  },
  "fr": {
    "title": "Gestion du système",
    "tab": {
      "backups": "Sauvegardes",
      "audits": "Journal d'audit"
    }
  },
  "id": {
    "title": "Manajemen Sistem",
    "tab": {
      "backups": "Data Cadangan",
      "audits": "Catatan Server Audit"
    }
  }
}
</i18n>
