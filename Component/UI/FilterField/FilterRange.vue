<template>
    <b-field
        label="Range"
        label-position="on-border"
    >
        <b-input
            v-model.lazy="rawValue.gte"
            placeholder="Min"
            @change.native="onRawValueChange"
        />
        <b-input
            v-model.lazy="rawValue.lte"
            placeholder="Max"
            @change.native="onRawValueChange"
        />
    </b-field>
</template>

<script lang="ts">
import UiFilterBase from '#/Core/Component/UI/FilterField/FilterBase.vue';
import { Component } from '@/intiv/core/Vue/Annotations';


@Component()
export default class UiFilterRange
    extends UiFilterBase
{

    public rawValue = {
        gte: '',
        lte: '',
    };

}
</script>
