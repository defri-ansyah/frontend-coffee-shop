<template>
  <div class="d-flex flex-column">
    <label :for="id" class="label">{{label}}</label>
    <input :type="type" :id="id" :placeholder="placeholder" class="placeholder input" @input="$emit('input', $event)" @focus="$emit('focus', $event)" @keyup="$emit('keyup', $event)" required>
  </div>
</template>

<script>
export default {
	name: 'InputAuth',
	props: ['id', 'type', 'placeholder', 'label']
}
</script>

<style lang="scss" scoped>

.input {
  height: 75px;
  border: 1px solid #4F5665;
  border-radius: 20px;
  padding: 0 30px;
  margin: 0 0 32px 0;

  font-family: Rubik;
  font-style: normal;
  font-weight: normal;
  font-size: 20px;
  // line-height: 24px;
  color: #353535;
}

.input:focus {
  outline: none;
}

.placeholder::placeholder {
  font-family: Rubik;
  font-style: normal;
  font-weight: normal;
  font-size: 20px;
  line-height: 24px;
  color: #9F9F9F;
}

.label {
  font-family: Rubik;
  font-style: normal;
  font-weight: bold;
  font-size: 20px;
  line-height: 24px;
  color: #4F5665;
}

</style>
