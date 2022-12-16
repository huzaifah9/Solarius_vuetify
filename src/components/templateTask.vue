<template>
    <v-app style="background-color:#FBF7F4">
        <v-container fluid >
            <v-row no-gutters style="height: 150px;">
                <v-col class="col-3 pt-3">
                    <div class="text-center d-flex flex-column align-center justify-center pa-2" flat tile>
                        <v-img 
                        lazy-src="../assets/logo.png"
                        src="../assets/logo.png"
                        width="40">
                        </v-img>
                        <h2 class="pt-2">SOLARIUS</h2>
                    </div>
                    <div>
                        <v-list style="background-color:#FBF7F4;font-weight: bold;">
                            <v-list-item-group
                                v-model="selectedItem"
                            >
                                <v-list-item
                                v-for="(item, i) in items"
                                :key="i"
                                >
                                <v-list-item-icon>
                                    <v-icon style="color: black;" v-text="item.icon"></v-icon>
                                </v-list-item-icon>
                                <v-list-item-content>
                                    <v-list-item-title v-text="item.text"></v-list-item-title>
                                </v-list-item-content>
                                </v-list-item>
                            </v-list-item-group>
                            <v-list-group 
                                value="true"
                                no-action
                                color="black"
                                >
                            <template v-slot:activator>
                                <v-list-item-icon>
                                    <v-icon style="color: black;">mdi-palette-swatch-variant</v-icon>
                                </v-list-item-icon>
                                <v-list-item-content>
                                <v-list-item-title style="color: black;">Resources</v-list-item-title>
                                </v-list-item-content>
                            </template>
                            
                                <v-list-item
                                v-for="(item, i) in subItems"
                                :key="i"
                                >
                                <v-list-item-icon>
                                    <v-icon style="color: black;" v-text="item.icons"></v-icon>
                                </v-list-item-icon>
                                <v-list-item-content>
                                    <v-list-item-title v-text="item.text"></v-list-item-title>
                                </v-list-item-content>
                                </v-list-item>
                            </v-list-group>
                            <v-list-item-group
                            v-modal="selectedItem"
                            >
                                <v-list-item>
                                <v-list-item-icon>
                                    <v-icon style="color: black;">mdi-cog</v-icon>
                                </v-list-item-icon>

                                <v-list-item-title>Settings</v-list-item-title>
                                </v-list-item>
                            </v-list-item-group>
                        </v-list>
                        <div class="d-flex flex-row align-end">
                            <v-btn
                            class="mx-2 mt-4"
                            fab
                            dark
                            small
                            color="black"
                            >
                                <v-icon dark>
                                    mdi-logout
                                </v-icon>
                            </v-btn>
                        <h4 style="font-weight:bold" class="pb-2">Logout</h4>
                        </div>
                    </div>
                </v-col>
                <v-col class="col-4 pt-3" style="background-color: white">
                    <div class="pa-2 ma-2" flat tile>
                        <div class="d-flex flex-row justify-start">
                            <h3>Today's Plan<span><small style="color:grey;font-weight: 300; display: block;">June 14th,2022</small></span></h3>
                            <v-spacer></v-spacer>
                            <v-btn
                            class=""
                            fab
                            dark
                            color="black"
                            >
                                <v-icon dark>
                                    mdi-plus
                                </v-icon>
                            </v-btn>
                        </div>
                        <div class="my-7">
                            <h2>Sustainable Development goals and health innovation</h2>
                        </div>

                        <div class="d-flex">    
                            <v-avatar>
                                <v-img class="rounded-circle" src="../assets/1.jpg" alt=""></v-img>
                            </v-avatar>
                            <v-avatar class="avatars">
                                <v-img class="rounded-circle" src="../assets/2.jpg" alt=""></v-img>
                            </v-avatar>
                            <v-avatar class="avatars">
                                <v-img class="rounded-circle" src="../assets/3.jpg" alt=""></v-img>
                            </v-avatar>
                            <v-avatar class="avatars">
                                <v-img class="rounded-circle" src="../assets/4.jpg" alt=""></v-img>
                            </v-avatar>
                            <v-avatar class="avatars">
                                <v-img class="rounded-circle" src="../assets/4.jpg" alt=""></v-img>
                            </v-avatar>
                            <v-divider class="mx-8"
                                vertical 
                                inset
                            ></v-divider>
                            <p><b>Medi Team meeting</b><span><small style="color:grey; display:block">13:30 - 14:50</small></span></p>
                        </div>
                        <div>
                            <v-container>
                                <v-row no-gutters class="ma-2">
                                    <v-col class="col-11 ma-2">
                                        <v-card
                                        class="pa-4"
                                        outlined
                                        tile
                                        >
                                            <div>
                                                <h4>Weekly Report</h4>
                                                <p>track your Performance</p>
                                                <v-btn class="mt-4"
                                                outlined
                                                color="black">
                                                    VIEW REPORT
                                                </v-btn>
                                            </div>
                                        </v-card>
                                    </v-col>
                                    <v-col class="col-5 ma-2">
                                        <v-card
                                        class="pa-4"
                                        outlined
                                        tile
                                        >
                                            <div class="text-center">
                                                <h4>Study 78x</h4>
                                                <v-icon color="black">
                                                    mdi-clock
                                                </v-icon> <b>In Progress</b>
                                            </div>
                                        </v-card>
                                    </v-col>
                                    <v-col class="col-5 ma-2">
                                        <v-card
                                        class="pa-4"
                                        outlined
                                        tile
                                        >
                                            <div class="text-center">
                                                <h4>Analyses</h4>
                                                <v-icon color="black">
                                                    mdi-check-circle
                                                </v-icon> <b>Completed</b>
                                            </div>
                                        </v-card>
                                    </v-col>
                                </v-row>
                            </v-container>
                        </div>
                    </div>
                </v-col>
                <v-col class="col-4 pt-3">
                    <div class="pa-2 d-flex flex-row justify-start ma-2" flat tile>
                        <h3>Monthly Pinned </h3><v-spacer></v-spacer><p style="color:grey">View all</p>
                    </div>
                    <div class="mt-4">
                        <v-container>
                            <v-row no-gutters>
                            <v-col class="col-12 mt-4">
                                <v-card
                                class="pa-2"
                                outlined
                                tile
                                >
                                    <div class="pa-2 d-flex flex-row justify-start">
                                        <small style="color: grey;">Next-gen-immuno</small><v-spacer></v-spacer>
                                        <small style="color:grey">5d</small>
                                    </div>
                                    <div class="pa-2">
                                        <h4>Multispecific liquids analysis</h4>
                                    </div>
                                    <div class="pa-2">
                                        <v-icon color="black">
                                            mdi-numeric-1-circle
                                        </v-icon> <b>New Feedback</b>
                                    </div>
                                </v-card>
                            </v-col>
                            <v-col class="col-12 mt-4">
                                <v-card
                                class="pa-2"
                                outlined
                                tile
                                >
                                    <div class="pa-2 d-flex flex-row justify-start">
                                        <small style="color: grey;">Harmony</small><v-spacer></v-spacer>
                                        <small style="color:grey">1h</small>
                                    </div>
                                    <div class="pa-2">
                                        <h4>Protein Characterization during childhood and pragnancy</h4>
                                    </div>
                                    <div class="pa-2">
                                        <v-icon color="black">
                                            mdi-alert-circle
                                        </v-icon> <b>Deadline is today</b>
                                    </div>
                                </v-card>
                            </v-col>
                            <v-col class="col-12 mt-4">
                                <v-card
                                class="pa-2"
                                outlined
                                tile
                                >
                                    <div class="pa-2 d-flex flex-row justify-start">
                                        <small style="color: grey;">pharmaceutical</small><v-spacer></v-spacer>
                                        <small style="color:grey">7h</small>
                                    </div>
                                    <div class="pa-2">
                                        <h4>Quick element dissolution testing</h4>
                                    </div>
                                    <div class="pa-2">
                                        <v-icon color="black">
                                            mdi-check-circle
                                        </v-icon> <b>Accepted</b>
                                    </div>
                                </v-card>
                            </v-col>
                            </v-row>
                        </v-container>
                    </div>
                </v-col>
                <v-col class="col-1 pt-3">
                    <div class="pa-2 text-center ma-3" flat tile>
                        <v-badge
                        bordered
                        top
                        color="deep-purple accent-4"
                        dot
                        offset-x="10"
                        offset-y="10"
                        >
                            <v-avatar size="60">
                                <v-img src="../assets/2.jpg"></v-img>
                            </v-avatar>
                        </v-badge>
                        <div>
                            <h4>Dr. Riddle <span><small style="color:grey; display:block">Scientist</small></span></h4>
                        </div>
                        <div class="d-flex flex-column justify-end align-center mt-12">
                            <v-btn
                            class="mx-2 mt-3"
                            fab
                            small
                            color="white"
                            >
                                <v-icon>
                                    mdi-pencil
                                </v-icon>
                            </v-btn>
                            <v-btn
                            class="mx-2 mt-3"
                            fab
                            small
                            color="white"
                            >
                                <v-icon>
                                    mdi-comment-processing
                                </v-icon>
                            </v-btn>
                            <v-btn
                            class="mx-2 mt-3"
                            fab
                            dark
                            color="black"
                            >
                                <v-icon dark>
                                    mdi-plus
                                </v-icon>
                            </v-btn>
                        </div>
                    </div>
                </v-col>
            </v-row>
        </v-container>
    </v-app>
</template>
<script>
  export default {
    data: () => ({
      selectedItem: 1,
    items: [
        { text: 'Dashboard', icon: 'mdi-view-dashboard' },
        { text: 'Education', icon: 'mdi-school' },
        ],
    subItems:[
        {text: 'Genetics 101' ,icons:'mdi-square'},
        {text: 'DNA Synthesis' ,icons:'mdi-square'},
        {text: 'Events' ,icons:'mdi-square'}
        ],
    }),
  }
</script>

<style>
.avatars {
    margin-left: -15px;
}
</style>