<script setup lang="ts">
import { Switch } from '@/components/ui/switch'
import { Tabs, TabsContent, TabsList, TabsTrigger } from '@/components/ui/tabs'
import { Card, CardContent, CardDescription, CardHeader, CardTitle } from '@/components/ui/card'

const editProfile = () => {
  // Your logic for handling the edit click goes here
  console.log('Edit clicked!')
}
</script>
<template>
  <div class="container lg:px-0 mx-auto">
    <div class="flex flex-col lg:flex-row justify-evenly">
      <Card
        class="sm:col-span-3 md:col-span-3 bg-[#F8F9FF] sm:items-center shadow-2xl mb-auto mr-auto"
      >
        <CardHeader>
          <CardTitle class="text-xl font-bold">Admin Profile</CardTitle>
          <CardDescription>
            <img
              class=""
              src="https://res.cloudinary.com/dufimctfc/image/upload/v1710684025/images1_wbbxb5.svg"
              alt="gradient"
            />
            <div class="flex justify-between px-6 my-2">
              <span class="text-sm lg:text-base text-[#020721]">Identity</span>
              <div class="flex">
                <img
                  class="max-w-[18.05px] max-h-[24px]"
                  src="https://res.cloudinary.com/dufimctfc/image/upload/v1714310908/edit-4-svgrepo-com_1_iy2nwu.svg"
                  alt="gradient"
                />
                <div class="flex justify-between px-6 py-4 space-x-2">
                  <span class="text-sm font-bold text-[#020721]">Identity</span>
                  <div class="flex">
                    <img
                      class=""
                      src="https://res.cloudinary.com/dufimctfc/image/upload/v1714310908/edit-4-svgrepo-com_1_iy2nwu.svg"
                      alt="gradient"
                    />
                    <span class="ml-2 text-sm font-medium text-gray-700"> Edit </span>
                  </div>
                </div>

                <Card
                  class="grid grid-cols-1 gap-4 px-4 py-4 mt-4 border border-gray-200 rounded-md sm:grid-cols-2"
                >
                  <dt class="text-sm font-medium text-gray-500">First Name</dt>
                  <dd class="text-sm text-gray-800">Demliade</dd>
                  <dt class="text-sm font-medium text-gray-500">Last Name</dt>

            <div class="flex justify-between px-6 my-2">
              <span class="text-sm lg:text-base text-[#020721]">Contact</span>
              <div class="flex">
                <img
                  class="max-w-[18.05px] max-h-[24px]"
                  src="https://res.cloudinary.com/dufimctfc/image/upload/v1714310908/edit-4-svgrepo-com_1_iy2nwu.svg"
                  alt="gradient"
                />
                <span class="text-sm font-medium text-[#02072199]">
                  <a href="#" @click="editProfile">Edit</a>
                </span>
              </div>
            </div>

                  <dt class="text-sm font-medium text-gray-500">Role</dt>
                  <dd class="text-sm text-gray-800">Cxperience</dd>

                  <dt class="text-sm font-medium text-gray-500">Birthday</dt>
                  <dd class="text-sm text-gray-800">July 28</dd>

                  <dt class="text-sm font-medium text-gray-500">Gender</dt>
                  <dd class="text-sm text-gray-800">Female</dd>

                  <dt class="text-sm font-medium text-gray-500">Joined</dt>
                  <dd class="text-sm text-gray-800">3 Aug 2023</dd>
                </Card>
                <div class="flex justify-between px-6 py-4 space-x-2">
                  <span class="text-sm text-[#020721] font-bold">Contact</span>
                  <div class="flex">
                    <img
                      class=""
                      src="https://res.cloudinary.com/dufimctfc/image/upload/v1714310908/edit-4-svgrepo-com_1_iy2nwu.svg"
                      alt="gradient"
                    />
                    <span class="ml-2 text-sm font-medium text-gray-700"> Edit </span>
                  </div>
                </div>
                <Card
                  class="grid grid-cols-1 gap-4 px-4 py-4 mt-4 border border-gray-200 rounded-md sm:grid-cols-2"
                >
                  <dt class="text-sm font-medium text-gray-500">Email</dt>
                  <dd class="text-sm text-gray-800">felixont@email.uk</dd>
                  <dt class="text-sm font-medium text-gray-500">phone.no</dt>
                  <dd class="text-sm text-gray-800">felixont@email.uk</dd>
                  <dt class="text-sm font-medium text-gray-500">Address</dt>
                  <dd class="text-sm text-gray-800">No. 51, Briswood Ipaja Rd, Ikeja</dd>
                  <p>User ID: {{ $route.params.userId }}</p>
                </Card>
              </CardDescription>
            </CardHeader>
          </Card>

          <div class="col-span-4 my-9">
            <Tabs default-value="permission" class="space-y-4">
              <TabsList class="text-blue-900">
                <TabsTrigger value="permission" class="text-[#000000]"> Permission </TabsTrigger>
                <TabsTrigger value="analytics" disabled> Activity log </TabsTrigger>
              </TabsList>
              <TabsContent value="permission" class="space-y-4">
                <div>
                  <Card Content class="bg-[#F8F9FF] mt-4">
                    <CardContent
                      class="flex flex-col items-center justify-between px-2 py-4 sm:flex-row sm:px-6"
                    >
                      <div
                        class="inline-block bg-[#373B4D] text-[#F8F9FF] rounded-full px-2 py-1 text-sm"
                      >
                        Dashboard
                      </div>
                      <p class="text-sm text-muted-foreground text-center text-[#000000]">
                        Get an overall stats of Weeshr and a users list at login
                      </p>
                      <Switch />
                    </CardContent>
                  </Card>

                  <Card Content class="bg-[#F8F9FF] mt-4">
                    <CardContent
                      class="flex flex-col items-center justify-between px-2 py-4 sm:flex-row sm:px-6"
                    >
                      <div
                        class="inline-block bg-[#373B4D] text-[#F8F9FF] rounded-full px-2 py-1 text-sm"
                      >
                        Users
                      </div>
                      <p class="text-sm text-muted-foreground text-center text-[#000000]">
                        View and manage all Weeshr app users,admin ,vendors and partners
                      </p>
                      <Switch />
                    </CardContent>
                  </Card>

                  <Card Content class="bg-[#F8F9FF] mt-4">
                    <CardContent
                      class="flex flex-col items-center justify-between px-2 py-4 sm:flex-row sm:px-6"
                    >
                      <div
                        class="inline-block bg-[#373B4D] text-[#F8F9FF] rounded-full px-2 py-1 text-sm"
                      >
                        Weeshes
                      </div>
                      <p class="text-sm text-muted-foreground text-center text-[#000000]">
                        View and manage all weeshes at different level fulfillement
                      </p>
                      <Switch />
                    </CardContent>
                  </Card>

                  <Card Content class="bg-[#F8F9FF] mt-4">
                    <CardContent
                      class="flex flex-col items-center justify-between px-2 py-4 sm:flex-row sm:px-6"
                    >
                      <div
                        class="inline-block bg-[#373B4D] text-[#F8F9FF] rounded-full px-2 py-1 text-sm"
                      >
                        Depot
                      </div>
                      <p class="text-sm text-muted-foreground text-center text-[#000000]">
                        Manage fulfilled weeshes and delievery status
                      </p>
                      <Switch />
                    </CardContent>
                  </Card>

                  <Card Content class="bg-[#F8F9FF] mt-4">
                    <CardContent
                      class="flex flex-col items-center justify-between px-2 py-4 sm:flex-row sm:px-6"
                    >
                      <div
                        class="inline-block bg-[#373B4D] text-[#F8F9FF] rounded-full px-2 py-1 text-sm"
                      >
                        Bank
                      </div>
                      <p class="text-sm text-muted-foreground text-center text-[#000000]">
                        View and manage funds in user's wallet
                      </p>
                      <Switch />
                    </CardContent>
                  </Card>

                  <Card Content class="bg-[#F8F9FF] mt-4">
                    <CardContent
                      class="flex flex-col items-center justify-between px-2 py-4 sm:flex-row sm:px-6"
                    >
                      <div
                        class="inline-block bg-[#373B4D] text-[#F8F9FF] rounded-full px-2 py-1 text-sm"
                      >
                        Support
                      </div>
                      <p class="text-sm text-muted-foreground text-center text-[#000000]">
                        View and manage tickets and complaints from users
                      </p>
                      <Switch />
                    </CardContent>
                  </Card>

                  <Card Content class="bg-[#F8F9FF] mt-4">
                    <CardContent
                      class="flex flex-col items-center justify-between px-2 py-4 sm:flex-row sm:px-6"
                    >
                      <div
                        class="inline-block bg-[#373B4D] text-[#F8F9FF] rounded-full px-2 py-1 text-sm"
                      >
                        Configuration
                      </div>
                      <p class="text-sm text-muted-foreground text-center text-[#000000]">
                        Manage the core engine of Weeshr
                      </p>
                      <Switch />
                    </CardContent>
                  </Card>

                  <Card Content class="bg-[#F8F9FF] mt-4">
                    <CardContent
                      class="flex flex-col items-center justify-between px-2 py-4 sm:flex-row sm:px-6"
                    >
                      <div
                        class="inline-block bg-[#373B4D] text-[#F8F9FF] rounded-full px-2 py-1 text-sm"
                      >
                        Analytics
                      </div>
                      <p class="text-sm text-muted-foreground text-center text-[#000000]">
                        Get general data in regards to Weeshr performance
                      </p>
                      <Switch />
                    </CardContent>
                  </Card>

                  <Card Content class="bg-[#F8F9FF] mt-4">
                    <CardContent
                      class="flex flex-col items-center justify-between px-2 py-4 sm:flex-row sm:px-6"
                    >
                      <div
                        class="inline-block bg-[#373B4D] text-[#F8F9FF] rounded-full px-2 py-1 text-sm"
                      >
                        Activity logs
                      </div>
                      <p class="text-sm text-muted-foreground text-center text-[#000000]">
                        View all activites of weeshr in record
                      </p>
                      <Switch />
                    </CardContent>
                  </Card>
                </div>
              </TabsContent>
            </Tabs>
          </div>
        </div>
      

      <div class="my-9 lg:mx-auto">
        <Tabs default-value="permission" class="space-y-1">
          <TabsList
            class="border-b-8 border-[#DEDFE8] lg:justify-between px-0 lg:px-6 md:px-6 py-2 bg-transparent"
          >
            <TabsTrigger value="permission" class="text-[#000000]"> Permission </TabsTrigger>
            <TabsTrigger value="analytics" disabled> Activity log </TabsTrigger>
          </TabsList>
          <TabsContent value="permission" class="space-y-4">
            <div class="lg:w-[802px]">
              <Card Content class="bg-[#F8F9FF] mt-4">
                <CardContent
                  class="flex flex-col sm:flex-row items-center justify-between px-2 sm:px-6 py-4"
                >
                  <div
                    class="inline-block bg-[#373B4D] text-[#F8F9FF] rounded-full px-2 py-1 text-sm"
                  >
                    Dashboard
                  </div>
                  <p class="text-sm text-muted-foreground text-center text-[#000000]">
                    Get an overall stats of Weeshr and a users list at login
                  </p>
                  <Switch />
                </CardContent>
              </Card>

              <Card Content class="bg-[#F8F9FF] mt-4">
                <CardContent
                  class="flex flex-col sm:flex-row items-center justify-between px-2 sm:px-6 py-4"
                >
                  <div
                    class="inline-block bg-[#373B4D] text-[#F8F9FF] rounded-full px-2 py-1 text-sm"
                  >
                    Users
                  </div>
                  <p class="text-sm text-muted-foreground text-center text-[#000000]">
                    View and manage all Weeshr app users,admin ,vendors and partners
                  </p>
                  <Switch />
                </CardContent>
              </Card>

              <Card Content class="bg-[#F8F9FF] mt-4">
                <CardContent
                  class="flex flex-col sm:flex-row items-center justify-between px-2 sm:px-6 py-4"
                >
                  <div
                    class="inline-block bg-[#373B4D] text-[#F8F9FF] rounded-full px-2 py-1 text-sm"
                  >
                    Weeshes
                  </div>
                  <p class="text-sm text-muted-foreground text-center text-[#000000]">
                    View and manage all weeshes at different level fulfillement
                  </p>
                  <Switch />
                </CardContent>
              </Card>

              <Card Content class="bg-[#F8F9FF] mt-4">
                <CardContent
                  class="flex flex-col sm:flex-row items-center justify-between px-2 sm:px-6 py-4"
                >
                  <div
                    class="inline-block bg-[#373B4D] text-[#F8F9FF] rounded-full px-2 py-1 text-sm"
                  >
                    Depot
                  </div>
                  <p class="text-sm text-muted-foreground text-center text-[#000000]">
                    Manage fulfilled weeshes and delievery status
                  </p>
                  <Switch />
                </CardContent>
              </Card>

              <Card Content class="bg-[#F8F9FF] mt-4">
                <CardContent
                  class="flex flex-col sm:flex-row items-center justify-between px-2 sm:px-6 py-4"
                >
                  <div
                    class="inline-block bg-[#373B4D] text-[#F8F9FF] rounded-full px-2 py-1 text-sm"
                  >
                    Bank
                  </div>
                  <p class="text-sm text-muted-foreground text-center text-[#000000]">
                    View and manage funds in user's wallet
                  </p>
                  <Switch />
                </CardContent>
              </Card>

              <Card Content class="bg-[#F8F9FF] mt-4">
                <CardContent
                  class="flex flex-col sm:flex-row items-center justify-between px-2 sm:px-6 py-4"
                >
                  <div
                    class="inline-block bg-[#373B4D] text-[#F8F9FF] rounded-full px-2 py-1 text-sm"
                  >
                    Support
                  </div>
                  <p class="text-sm text-muted-foreground text-center text-[#000000]">
                    View and manage tickets and complaints from users
                  </p>
                  <Switch />
                </CardContent>
              </Card>

              <Card Content class="bg-[#F8F9FF] mt-4">
                <CardContent
                  class="flex flex-col sm:flex-row items-center justify-between px-2 sm:px-6 py-4"
                >
                  <div
                    class="inline-block bg-[#373B4D] text-[#F8F9FF] rounded-full px-2 py-1 text-sm"
                  >
                    Configuration
                  </div>
                  <p class="text-sm text-muted-foreground text-center text-[#000000]">
                    Manage the core engine of Weeshr
                  </p>
                  <Switch />
                </CardContent>
              </Card>

              <Card Content class="bg-[#F8F9FF] mt-4">
                <CardContent
                  class="flex flex-col sm:flex-row items-center justify-between px-2 sm:px-6 py-4"
                >
                  <div
                    class="inline-block bg-[#373B4D] text-[#F8F9FF] rounded-full px-2 py-1 text-sm"
                  >
                    Analytics
                  </div>
                  <p class="text-sm text-muted-foreground text-center text-[#000000]">
                    Get general data in regards to Weeshr performance
                  </p>
                  <Switch />
                </CardContent>
              </Card>

              <Card Content class="bg-[#F8F9FF] mt-4">
                <CardContent
                  class="flex flex-col sm:flex-row items-center justify-between px-2 sm:px-6 py-4"
                >
                  <div
                    class="inline-block bg-[#373B4D] text-[#F8F9FF] rounded-full px-2 py-1 text-sm"
                  >
                    Activity logs
                  </div>
                  <p class="text-sm text-muted-foreground text-center text-[#000000]">
                    View all activites of weeshr in record
                  </p>
                  <Switch />
                </CardContent>
              </Card>
            </div>
          </TabsContent>
        </Tabs>
      </div>
    </div>
  
</template>