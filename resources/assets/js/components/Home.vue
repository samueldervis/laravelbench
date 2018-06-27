<template>
    <div>
        <v-toolbar
                dense
                color="primary"
                dark
                extended
                extension-height="300"
                flat
        >
            <v-toolbar-title class="mx-auto" slot="extension">
                <span>Mobile Money API Visualization</span>
                <h2>Works with ...</h2>
                <v-layout row>
                    <v-flex wrap>
                        <v-btn outline large fab color="white" class="outine-2">
                            <i class="fab fa-laravel fa-2x"></i>
                        </v-btn>
                    </v-flex>
                    <v-flex wrap>
                        <v-btn outline large fab color="white" class="outine-2">
                            <i class="fab fa-react fa-3x"></i>
                        </v-btn>
                    </v-flex>
                    <v-flex wrap>
                        <v-btn outline large fab color="white" class="outine-2">
                            <i class="fab fa-vuejs fa-3x"></i>
                        </v-btn>
                    </v-flex>
                </v-layout>
            </v-toolbar-title>
        </v-toolbar>

        <v-container>
            <v-layout row>
                <v-flex xs12 md8 offset-md2>
                    <v-card flat class="card--flex-toolbar" color="transparent">
                        <v-container fluid grid-list-lg>
                            <v-layout row wrap>
                                <v-flex xs12>
                                    <h2 class="white--text">Discover our expressive API</h2>
                                </v-flex>
                            </v-layout>
                            <v-layout row wrap>
                                <v-flex xs12 sm6 md6 lg4 v-for="item in links" :key="item.id">
                                    <v-card>
                                        <v-card-media
                                                src=""
                                                height="125px"
                                                :class="item.color"
                                        >
                                        </v-card-media>
                                        <v-card-title primary-title>
                                            <div>
                                                <h3 class="headline mb-0">{{item.title}}</h3>
                                                <div>
                                                    {{item.description}}
                                                </div>
                                            </div>
                                        </v-card-title>
                                        <v-card-actions>
                                            <!--<v-btn flat color="primary" class="learn-more-btn">Learn more</v-btn>-->
                                            <v-spacer></v-spacer>
                                            <v-btn flat color="primary">Get started</v-btn>
                                        </v-card-actions>
                                    </v-card>
                                </v-flex>
                            </v-layout>
                        </v-container>
                    </v-card>
                </v-flex>
            </v-layout>
        </v-container>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                links: [
                    {
                        id: '1',
                        title: 'MPESA',
                        description: 'The most common payment method with large customer base',
                        color: 'green'
                    },
                    {
                        id: '2',
                        title: 'Airtel Money',
                        description: 'Artel Money has been there for sometime, cheap transactions.',
                        color: 'red'
                    },
                    {
                        id: '3',
                        title: 'Equitel',
                        description: 'Equity\'s mobile money payment platform',
                        color: 'teal'
                    },
                    {
                        id: '4',
                        title: 'T-Cash',
                        description: 'Telkom Kenya\'s API',
                        color: 'orange'
                    }
                ]
            }
        }
    }
</script>

<style scoped>
    .outine-2 {
        border: 2px solid white;
    }

    .card--flex-toolbar {
        margin-top: -104px;
    }

    .learn-more-btn {
        text-transform: initial;
        text-decoration: underline;
    }
</style>