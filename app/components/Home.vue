<template>
    <Page>
        <ActionBar id="actionBar" flat="true">
            <Label text="Trenitaly"></Label>
        </ActionBar>

        <GridLayout rows="200 *">
            <GridLayout row="0" id="input-form-grid">
                <GridLayout rows="auto auto auto auto auto">        
                    <GridLayout row="0" id="station-textfield-container" columns="* auto">            
                        <StackLayout column="0">
                            <TextField id="departure-station" hint="Departure" />
                            <TextField id="arrival-station" hint="Arrival" />
                        </StackLayout>
                        <StackLayout column="1" id="station-reverser-container">
                            <Button text="⤤⤦" />
                        </StackLayout>
                    </GridLayout>

                    <Button row="4" text="Search" />
                </GridLayout>
            </GridLayout>
        </GridLayout>
    </Page>
</template>

<script>
    export default {
    };
</script>

<style scoped lang="scss">
    $red: #c0392b;
    $darker-red: darken($red, 10%);
    $lighter-red: lighten($red, 5%);

    #actionBar {
        background-color: $red;
    }
    #input-form-grid {
        background-color: $lighter-red;

        #station-textfield-container {
            textfield {
                &#departure-station {
                    margin-bottom: 0px;
                    border-right-color: transparent;
                }
                &#arrival-station {
                    margin-top: 0px;
                    border-color: transparent;
                }
                background-color: $darker-red;
                padding: 24px;
            }
        }

        #station-reverser-container {
            vertical-align: center;
            button {
                margin-left: 0px;
                font-size: 24px;
            }
        }

        button {
            background-color: $darker-red;
        }
    }
</style>
