<script type="text/ecmascript-6">
    import Launch from './launch.vue';

    export default {
        components: {Launch}
    }
</script>

<template>
    <div class="testtest">
        <custom-index-screen title="Tasks" resource="tasks">
            <tr slot="table-header">
                <th scope="col">Domain</th>
                <th scope="col">Repo</th>
                <th scope="col">Branch</th>
                <th scope="col">Server</th>
                <th scope="col"></th>
            </tr>

            <template slot="row" slot-scope="slotProps">
                <td class="table-fit">
                    {{ slotProps.entry[0].domain }}
                </td>

                <td class="table-fit">
                    {{ slotProps.entry[0].repo }}
                </td>

                <td class="table-fit">
                    {{ slotProps.entry[0].branch }}
                </td>

                <td class="table-fit">
                    {{ slotProps.entry[0].server }}
                </td>

                <td class="table-fit">
                    <Launch :repo="slotProps.entry[0].repo" :branch="slotProps.entry[0].branch" />
                </td>

            </template>
        </custom-index-screen>
    </div>

</template>
