<template>
  <div class="settings-fields">
    <section class="box box--items">
      <div class="box__content">
        <box-item
          label="Upload mode."
          description="The uploaded photos will be added to the selected section.">
          <select v-model="currentValue.app.uploadMode" class="input">
            <option value="none">
              Pending
            </option>
            <option value="go-preferences">
              Pending -> Preferences
            </option>
            <option value="add-queue">
              Queue
            </option>
          </select>
        </box-item>

        <box-item
          label="Hardware Acceleration"
          description="It can improve performance on some systems. (Requires restart to take effect)">
          <select v-model="currentValue.app.disableHardwareAcceleration" class="input">
            <option :value="false">
              Enabled
            </option>
            <option :value="true">
              Disabled
            </option>
          </select>
        </box-item>

        <box-item
          label="Queue position."
          description="Change the position of the queue bar to the place that is most comfortable for you.">
          <select v-model="currentValue.app.queuePosition" class="input">
            <option value="right">
              Right
            </option>
            <option value="left">
              Left
            </option>
          </select>
        </box-item>
      </div>
    </section>
  </div>
</template>

<script>
import { VModel } from '~/mixins'

export default {
  mixins: [VModel],
}
</script>
