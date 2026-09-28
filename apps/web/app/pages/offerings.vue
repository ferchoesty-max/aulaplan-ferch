<script setup lang="ts">
import type { CatalogField } from '~/types'

const fields: CatalogField[] = [
  { key: 'academic_period_id', label: 'ID periodo', type: 'text', required: true },
  { key: 'subject_id', label: 'ID materia', type: 'text', required: true },
  { key: 'group_id', label: 'ID grupo', type: 'text', required: true },
  { key: 'teacher_id', label: 'ID profesor', type: 'text', required: true },
  { key: 'active', label: 'Activo', type: 'checkbox', required: false, defaultValue: true },
]
</script>

<template>
  <CatalogManager title="Ofertas académicas" endpoint="/offerings" :fields="fields" />
</template>
