<template>
  <q-page class="q-pa-md bg-secondary">
    <div class="row q-px-md q-py-md">
        <h5 class="text-white  text-left">
          Hello, Test
        </h5>
      </div>

    <!-- <card-social icon_position="left"/> -->

    <card-charts/>

    <div class="row q-col-gutter-sm  q-pb-sm">
      <todo-list/>

      <card-time-line/>
    </div>
  <!-- <q-card class="q-mt-md row bg-primary">
      <q-card-section class="col-12 text-center q-pa-lg">

        <div class="text-body1 q-mt-sm text-grey-7 text-weight-bold">
          © 2020 Davi Coscarelli, Inc. All rights reserved.
        </div>
      </q-card-section>
    </q-card> -->
  </q-page>
</template>

<script>
import {defineComponent,defineAsyncComponent} from 'vue'

export default defineComponent({
  name: 'PageIndex',
  components: {
    CardSocial: defineAsyncComponent(() => import('components/cards/CardSocial')),
    CardCharts: defineAsyncComponent(() => import('components/cards/CardCharts')),
    // CardCharts: () => import('components/cards/CardCharts'),
    TabSocial: defineAsyncComponent(() => import('components/tabs/TabSocial')),
    CardWithImage: defineAsyncComponent(() => import('components/cards/CardWithImage')),
    CardTimeLine: defineAsyncComponent(() => import('components/cards/CardTimeLine')),
    TodoList: defineAsyncComponent(() => import('components/list/TodoList')),
    TableVisits: defineAsyncComponent(() => import('components/tables/TableVisits')),
  },
  setup() {
    return {
      mode: 'list',
      messages: [
        {
          id: 5,
          name: 'Pratik Patel',
          msg: ' -- I\'ll be in your neighborhood doing errands this\n' +
            '            weekend. Do you want to grab brunch?',
          avatar: 'https://avatars2.githubusercontent.com/u/34883558?s=400&v=4',
          time: '10:42 PM'
        }, {
          id: 6,
          name: 'Winfield Stapforth',
          msg: ' -- I\'ll be in your neighborhood doing errands this\n' +
            '            weekend. Do you want to grab brunch?',
          avatar: 'https://cdn.quasar.dev/img/avatar6.jpg',
          time: '11:17 AM'
        }, {
          id: 1,
          name: 'Boy',
          msg: ' -- I\'ll be in your neighborhood doing errands this\n' +
            '            weekend. Do you want to grab brunch?',
          avatar: 'https://cdn.quasar.dev/img/boy-avatar.png',
          time: '5:17 AM'
        }, {
          id: 2,
          name: 'Jeff Galbraith',
          msg: ' -- I\'ll be in your neighborhood doing errands this\n' +
            '            weekend. Do you want to grab brunch?',
          avatar: 'https://cdn.quasar.dev/team/jeff_galbraith.jpg',
          time: '5:17 AM'
        }, {
          id: 3,
          name: 'Razvan Stoenescu',
          msg: ' -- I\'ll be in your neighborhood doing errands this\n' +
            '            weekend. Do you want to grab brunch?',
          avatar: 'https://cdn.quasar.dev/team/razvan_stoenescu.jpeg',
          time: '5:17 AM'
        }
      ],
    }
  },

})
</script>
