<template>
     <section class="py-8">
        <div class="container px-4 mx-auto">
          <div class="flex flex-wrap -mx-4">
            <div class="w-full lg:w-1/1 px-4 mb-8 lg:mb-0">
              <div class="pt-4 bg-white rounded">
                <div class="px-6 border-b border-blue-50">
                  <div class="flex flex-wrap items-center mb-4">
                    <div>
                      <h3 class="text-xl font-bold">-Star Wars Listing Table- </h3>
                    </div>
                  </div>
                  <div>
                    <span
                      v-on:click="change('table')"
                      :class="type === 'table' ? 'text-indigo-500 border-b-2 border-indigo-500' : 'text-gray-400 border-b-2 border-transparent hover:border-gray-300 cursor-pointer'"
                      class="inline-block px-4 pb-2 text-sm font-medium"
                    >Table View</span>
                    <span
                      v-on:click="change('graph')"
                      :class="type === 'graph' ? 'text-indigo-500 border-b-2 border-indigo-500' : 'text-gray-400 border-b-2 border-transparent hover:border-gray-300 cursor-pointer'"
                      class="inline-block px-4 pb-2 text-sm font-medium"
                    >Graph View</span>
                  </div>
                  <div v-if="type ==='table'">
                    <div class="flex gap-4" >
                      <div class="flex my-5 font-light rounded-md border-2 border-indigo-500 " role="button" @click="nameChecked = !nameChecked">
                        <span class="px-4 flex ">name
                          <div class="flex my-1 mx-1" v-if="nameChecked">
                              <svg  xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" viewBox="0 0 20 20" fill="currentColor">
                            <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                          </svg>
                        </div>
                        </span>
                      </div>
                      <div class="flex my-5 font-light rounded-md border-2 border-indigo-500 " role="button" @click="heightChecked = !heightChecked">
                        <span class="px-4 flex">height
                          <div class="flex my-1 mx-1" v-if="heightChecked">
                              <svg  xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" viewBox="0 0 20 20" fill="currentColor">
                            <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                          </svg>
                        </div>
                        </span>
                      </div>
                      <div class="flex my-5 font-light rounded-md border-2 border-indigo-500 " role="button" @click="massChecked = !massChecked">
                        <span class="px-4 flex">mass
                          <div class="flex my-1 mx-1" v-if="massChecked">
                              <svg  xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" viewBox="0 0 20 20" fill="currentColor">
                            <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                          </svg>
                        </div>
                        </span>
                      </div>
                      <div class="flex my-5 font-light rounded-md border-2 border-indigo-500 " role="button" @click="birthYearChecked = !birthYearChecked">
                        <span class="px-4 flex">birth year
                          <div class="flex my-1 mx-1" v-if="birthYearChecked">
                              <svg  xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" viewBox="0 0 20 20" fill="currentColor">
                            <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                          </svg>
                        </div>
                        </span>
                      </div>
                      <div class="flex my-5 font-light rounded-md border-2 border-indigo-500 " role="button" @click="genderChecked = !genderChecked">
                        <span class="px-4 flex">gender
                          <div class="flex my-1 mx-1" v-if="genderChecked">
                              <svg  xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" viewBox="0 0 20 20" fill="currentColor">
                            <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                          </svg>
                        </div>
                        </span>
                      </div>
                      <div class="flex my-5 font-light rounded-md border-2 border-indigo-500 " role="button" @click="homeworldChecked = !homeworldChecked">
                        <span class="px-4 flex">homeworld
                          <div class="flex my-1 mx-1" v-if="homeworldChecked">
                              <svg  xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" viewBox="0 0 20 20" fill="currentColor">
                            <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                          </svg>
                        </div>
                        </span>
                      </div>
                      <div class="flex my-5 font-light rounded-md border-2 border-indigo-500">
                        <span class="px-4 flex mx-2">Search
                          <div class="flex my-1 mx-1">
                              <input class=" mx-2 h-4 text-sm rounded-sm border border-transparent focus:outline-none focus:ring-2 focus:ring-indigo-60 focus:border-transparent" type="text" placeholder="Filter by name"  v-model="searchQuery" />
                          </div>
                        </span>
                      </div>
                    </div>
                  </div>
                  <div v-else >
                      <div class="flex gap-4" >
                      <div class="flex my-5 font-light rounded-md border-2 border-indigo-500 " role="button" @click="homeNameChecked = !homeNameChecked">
                        <span class="px-4 flex ">name
                          <div class="flex my-1 mx-1" v-if="homeNameChecked">
                              <svg  xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" viewBox="0 0 20 20" fill="currentColor">
                            <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                          </svg>
                        </div>
                        </span>
                      </div>
                      <div class="flex my-5 font-light rounded-md border-2 border-indigo-500 " role="button" @click="rotationPeriodChecked = !rotationPeriodChecked">
                        <span class="px-4 flex">rotation period
                          <div class="flex my-1 mx-1" v-if="rotationPeriodChecked">
                              <svg  xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" viewBox="0 0 20 20" fill="currentColor">
                            <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                          </svg>
                        </div>
                        </span>
                      </div>
                      <div class="flex my-5 font-light rounded-md border-2 border-indigo-500 " role="button" @click="orbitalPeriodChecked = !orbitalPeriodChecked">
                        <span class="px-4 flex">orbital period
                          <div class="flex my-1 mx-1" v-if="orbitalPeriodChecked">
                              <svg  xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" viewBox="0 0 20 20" fill="currentColor">
                            <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                          </svg>
                        </div>
                        </span>
                      </div>
                      <div class="flex my-5 font-light rounded-md border-2 border-indigo-500 " role="button" @click="diameterChecked = !diameterChecked">
                        <span class="px-4 flex">diameter
                          <div class="flex my-1 mx-1" v-if="diameterChecked">
                              <svg  xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" viewBox="0 0 20 20" fill="currentColor">
                            <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                          </svg>
                        </div>
                        </span>
                      </div>
                      <div class="flex my-5 font-light rounded-md border-2 border-indigo-500 " role="button" @click="climateChecked = !climateChecked">
                        <span class="px-4 flex">climate
                          <div class="flex my-1 mx-1" v-if="climateChecked">
                              <svg  xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" viewBox="0 0 20 20" fill="currentColor">
                            <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                          </svg>
                        </div>
                        </span>
                      </div>
                      <div class="flex my-5 font-light rounded-md border-2 border-indigo-500 " role="button" @click="gravityChecked = !gravityChecked">
                        <span class="px-4 flex">gravity
                          <div class="flex my-1 mx-1" v-if="gravityChecked">
                              <svg  xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" viewBox="0 0 20 20" fill="currentColor">
                            <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                          </svg>
                        </div>
                        </span>
                      </div>
                      <div class="flex my-5 font-light rounded-md border-2 border-indigo-500 " role="button" @click="terrainChecked = !terrainChecked">
                        <span class="px-4 flex">terrain
                          <div class="flex my-1 mx-1" v-if="terrainChecked">
                              <svg  xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" viewBox="0 0 20 20" fill="currentColor">
                            <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                          </svg>
                        </div>
                        </span>
                      </div>
                      <div class="flex my-5 font-light rounded-md border-2 border-indigo-500 " role="button" @click="surfaceWaterChecked = !surfaceWaterChecked">
                        <span class="px-4 flex">surface water
                          <div class="flex my-1 mx-1" v-if="surfaceWaterChecked">
                              <svg  xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" viewBox="0 0 20 20" fill="currentColor">
                            <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                          </svg>
                        </div>
                        </span>
                      </div>
                      <div class="flex my-5 font-light rounded-md border-2 border-indigo-500 " role="button" @click="populationChecked = !populationChecked">
                        <span class="px-4 flex">population
                          <div class="flex my-1 mx-1" v-if="populationChecked">
                              <svg  xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" viewBox="0 0 20 20" fill="currentColor">
                            <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                          </svg>
                        </div>
                        </span>
                      </div>
                    </div>
                </div>
                <div>
                    </div>
                  </div>
                </div>
                <div>
                    <table v-if="type === 'table'" class="border-collapse w-full">
                    <thead class="bg-gray-50">
                      <tr class="border-b text-sm border-blue-50">
                        <th class="p-3 text-gray-500 hidden lg:table-cell" v-if="nameChecked">name</th>
                        <th class="p-3 text-gray-500 hidden lg:table-cell" v-if="heightChecked">height</th>
                        <th class="p-3 text-gray-500 hidden lg:table-cell" v-if="massChecked">mass</th>
                        <th class="p-3 text-gray-500 hidden lg:table-cell" v-if="birthYearChecked">birth year</th>
                        <th class="p-3 text-gray-500 hidden lg:table-cell" v-if="genderChecked">gender</th>
                        <th class="p-3 text-gray-500 hidden lg:table-cell" v-if="homeworldChecked">homeworld</th>
                      </tr>
                    </thead>
                    <tbody>
                      <tr v-for="item in resultQuery" :key="item.id">
                        <td  v-if="nameChecked" class="w-full lg:w-auto text-gray-800 text-center border-b block lg:table-cell relative lg:static">
                          <span class="lg:hidden static text-indigo-600 px-2 py-1 text-xs border-b font-bold">name</span><br class="mb-2">
                          <p class="py-1 px-2 text-sm">{{item.name}}</p>
                        </td>
                        <td v-if="heightChecked" class="w-full lg:w-auto text-gray-800 text-center border-b block lg:table-cell relative lg:static">
                                <span class="lg:hidden static text-indigo-600 px-2 py-1 text-xs border-b font-bold">height</span><br class="mb-2">
                                <p class="py-1 px-2 text-sm">{{item.height}}</p>
                            </td>
                            <td v-if="massChecked" class="w-full lg:w-auto text-gray-800 text-center border-b block lg:table-cell relative lg:static">
                                <span class="lg:hidden static text-indigo-600 px-2 py-1 text-xs border-b font-bold w-24">mass</span><br class="mb-2">
                                <p class="py-1 px-2 text-sm mx-4 pt-2">{{item.mass}}</p>
                            </td>
                            <td v-if="birthYearChecked" class="w-full lg:w-auto text-gray-800 text-center border-b block lg:table-cell relative lg:static">
                                <span class="lg:hidden static text-indigo-600 px-2 py-1 text-xs border-b font-bold w-24">birth year</span><br class="mb-2">
                                <span class="py-1 px-2 text-xs text-yellow-500 rounded-full lg:flex xl:flex lg:justify-center xl:justify-center"> {{item.birth_year}} </span>
                            </td>
                            <td v-if="genderChecked" class="w-full lg:w-auto text-gray-800 text-center border-b block lg:table-cell relative lg:static">
                                <span class="lg:hidden static text-indigo-600 px-2 py-1 text-xs border-b font-bold w-24">gender</span><br class="mb-2">
                                <span class="py-1 px-2 text-blue-400 hover:text-blue-600 text-xs ">{{item.gender}}</span>
                            </td>
                            <td v-if="homeworldChecked" class="w-full lg:w-auto text-gray-800 text-center border-b block lg:table-cell relative lg:static">
                                <span class="lg:hidden static text-indigo-600 px-2 py-1 text-xs border-b font-bold w-24">homeworld</span><br class="mb-2">
                                <span v-for="home in homeworld.results" :key="home.id" class="py-1 px-2 text-sm">
                                    <p v-if="home.url == item.homeworld">
                                      <button class="border border-indigo-600 rounded-md text-green-400 hover:text-green-600 hover:border-indigo-800 " @click="viewHome(home)"  >
                                        <p class="p-1">{{home.name}}</p>
                                      </button>
                                    </p>
                                </span>
                            </td>
                    </tr>
                      
                    </tbody>
                  </table>
                  <div>
                  </div>
                    <div v-if="type === 'graph'" class="border-collapse w-full">
                      <div class="flex justify-center mt-8">
                          <table class="border-collapse w-full">
                              <thead class="bg-gray-50">
                                <tr class="border-b text-sm border-blue-50">
                                  <th class="p-3 text-gray-500 hidden lg:table-cell" v-if="homeNameChecked">name</th>
                                  <th class="p-3 text-gray-500 hidden lg:table-cell" v-if="rotationPeriodChecked">rotation period</th>
                                  <th class="p-3 text-gray-500 hidden lg:table-cell" v-if="orbitalPeriodChecked">orbital period</th>
                                  <th class="p-3 text-gray-500 hidden lg:table-cell" v-if="diameterChecked">diameter</th>
                                  <th class="p-3 text-gray-500 hidden lg:table-cell" v-if="climateChecked">climate</th>
                                  <th class="p-3 text-gray-500 hidden lg:table-cell" v-if="gravityChecked">gravity</th>
                                  <th class="p-3 text-gray-500 hidden lg:table-cell" v-if="terrainChecked">terrain</th>
                                  <th class="p-3 text-gray-500 hidden lg:table-cell" v-if="surfaceWaterChecked">surface water</th>
                                  <th class="p-3 text-gray-500 hidden lg:table-cell" v-if="populationChecked">population</th>
                                </tr>
                              </thead>
                              <tbody>
                                <tr :key="home">
                                  <td  v-if="homeNameChecked" class="w-full lg:w-auto text-gray-800 text-center border-b block lg:table-cell relative lg:static">
                                    <span class="lg:hidden static text-indigo-600 px-2 py-1 text-xs border-b font-bold">name</span><br class="mb-2">
                                    <p class="py-1 px-2 text-sm">{{name}}</p>
                                  </td>
                                  <td v-if="rotationPeriodChecked" class="w-full lg:w-auto text-gray-800 text-center border-b block lg:table-cell relative lg:static">
                                          <span class="lg:hidden static text-indigo-600 px-2 py-1 text-xs border-b font-bold">rotation period</span><br class="mb-2">
                                          <p class="py-1 px-2 text-sm">{{rotation_period}}</p>
                                      </td>
                                      <td v-if="orbitalPeriodChecked" class="w-full lg:w-auto text-gray-800 text-center border-b block lg:table-cell relative lg:static">
                                          <span class="lg:hidden static text-indigo-600 px-2 py-1 text-xs border-b font-bold w-24">orbital period</span><br class="mb-2">
                                          <p class="py-1 px-2 text-sm mx-4 pt-2">{{orbital_period}}</p>
                                      </td>
                                      <td v-if="diameterChecked" class="w-full lg:w-auto text-gray-800 text-center border-b block lg:table-cell relative lg:static">
                                          <span class="lg:hidden static text-indigo-600 px-2 py-1 text-xs border-b font-bold w-24">diameter</span><br class="mb-2">
                                          <span class="py-1 px-2 text-xs text-yellow-500 rounded-full lg:flex xl:flex lg:justify-center xl:justify-center"> {{diameter}} </span>
                                      </td>
                                      <td v-if="climateChecked" class="w-full lg:w-auto text-gray-800 text-center border-b block lg:table-cell relative lg:static">
                                          <span class="lg:hidden static text-indigo-600 px-2 py-1 text-xs border-b font-bold w-24">climate</span><br class="mb-2">
                                          <span class="py-1 px-2 text-blue-400 hover:text-blue-600 text-xs ">{{climate}}</span>
                                      </td>
                                      <td v-if="gravityChecked" class="w-full lg:w-auto text-gray-800 text-center border-b block lg:table-cell relative lg:static">
                                          <span class="lg:hidden static text-indigo-600 px-2 py-1 text-xs border-b font-bold w-24">gravity</span><br class="mb-2">
                                          <span class="py-1 px-2 text-yellow-400 hover:text-yellow-600 text-xs ">{{gravity}}</span>
                                      </td>
                                      <td v-if="terrainChecked" class="w-full lg:w-auto text-gray-800 text-center border-b block lg:table-cell relative lg:static">
                                          <span class="lg:hidden static text-indigo-600 px-2 py-1 text-xs border-b font-bold w-24">terrain</span><br class="mb-2">
                                          <span class="py-1 px-2 text-purple-400 hover:text-purple-600 text-xs ">{{terrain}}</span>
                                      </td>
                                      <td v-if="surfaceWaterChecked" class="w-full lg:w-auto text-gray-800 text-center border-b block lg:table-cell relative lg:static">
                                          <span class="lg:hidden static text-indigo-600 px-2 py-1 text-xs border-b font-bold w-24">surface water</span><br class="mb-2">
                                          <span class="py-1 px-2 text-pink-400 hover:text-pink-600 text-xs ">{{surface_water}}</span>
                                      </td>
                                      <td v-if="populationChecked" class="w-full lg:w-auto text-gray-800 text-center border-b block lg:table-cell relative lg:static">
                                          <span class="lg:hidden static text-indigo-600 px-2 py-1 text-xs border-b font-bold w-24">population</span><br class="mb-2">
                                          <span class="py-1 px-2 text-green-400 hover:text-green-600 text-xs ">{{population}}</span>
                                      </td>
                              </tr>
                              </tbody>
                            </table>
                      </div>
                    </div>
                </div>
              </div>
            </div>
          </div>
  </section>
</template>

<script>
import axios from 'axios'

export default {
  name: 'mainComponent',
  components: {
  },
  data () {
    return {
      type: 'table',
      dataSet: [],
      searchQuery: null,
      homeworld: [],
      nameChecked : true,
      heightChecked : true,
      massChecked : true,
      birthYearChecked : true,
      genderChecked : true,
      homeworldChecked : true,
      homeNameChecked : true,
      rotationPeriodChecked : true,
      orbitalPeriodChecked : true,
      diameterChecked : true,
      climateChecked : true,
      gravityChecked : true,
      terrainChecked : true,
      surfaceWaterChecked : true,
      populationChecked : true,
      resources:[]
    }
  },
  mounted: function() {
    console.log(this.checkedFilters)
    axios.get('https://swapi.dev/api/people/')
      .then(response => {
        this.dataSet = response.data;
        this.resources = this.dataSet.results;
      })
      .catch(error => {
        console.log(error);
      });
      axios.get('https://swapi.dev/api/planets/')
      .then(response => {
        this.homeworld = response.data;
        console.log(this.homeworld)
      })
      .catch(error => {
        console.log(error);
      });
  },
 computed: {
    resultQuery(){
      if(this.searchQuery){
      return this.resources.filter((item)=>{
        return this.searchQuery.toLowerCase().split(' ').every(v => item.name.toLowerCase().includes(v))
      })
      }else{
        return this.resources;
      }
    }
  },
  methods: {
    change (type) {
      this.type = type
    },
    viewHome(home) {
      this.type = 'graph'
      this.name = home.name
      this.rotation_period = home.rotation_period
			this.orbital_period = home.orbital_period
			this.diameter = home.diameter
			this.climate = home.climate
			this.gravity = home.gravity
			this.terrain = home.terrain
			this.surface_water = home.surface_water
			this.population = home.population
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
