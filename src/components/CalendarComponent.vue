<template>
    <div>
  <b-navbar toggleable="lg" type="dark">

    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav>
        <b-nav-item-dropdown text="Маршруты">
          <b-dropdown-item href="#">Маршруты </b-dropdown-item>
        </b-nav-item-dropdown>
        <b-nav-item-dropdown text="Календарь">
          <b-dropdown-item href="#">Календарь</b-dropdown-item>
        </b-nav-item-dropdown>
      </b-navbar-nav>

      <!-- Right aligned nav items -->
      <b-navbar-nav class="ml-auto">
        <b-nav-item right><font-awesome-icon icon="bell" size="lg" /></b-nav-item>
        <span class="badge">99+</span>
        <b-nav-item right>
          <font-awesome-icon icon="user" size="lg" style="margin-right: 10px"/>
          <span style="margin-right: 10px">4774</span>
        <font-awesome-icon icon="angle-down" size="lg" />
        </b-nav-item>
        
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
  <b-container fluid>
    <div class="content">
      <div class="left-content-wrap">
        <div class="breadcrumbs">
            <b-row>  
                <span class="breadcrumbs-text">Главная</span>
                <span class="breadcrumbs-delimiter">/</span>
                <span class="breadcrumbs-text__disabled">Маршруты по дням</span>
            </b-row>
        </div>
        <h1 class="title-text">Маршруты по дням</h1>
    <div class="calendar-settings">
      <div class="settings"> 
        <span><font-awesome-icon icon="plus" size="lg" /> Добавить маршрут</span>
            <span>Показать за месяц:
              <b-dropdown text="Месяц" class="text-o">
                  <b-dropdown-item href="#">Месяц</b-dropdown-item>
              </b-dropdown>
            </span>
        </div>
    </div>
    <div class="calendar-controller">
        <span class="calendar-controller-text"><font-awesome-icon icon="angle-left" /> Февраль 2018 <font-awesome-icon icon="angle-right" /></span>
    </div>
    <div class="main-content">
      <div class="large-calendar">
    <table class="table">
        <thead>
          <tr>
            <th>пн</th>
            <th>вт</th>
            <th>ср</th>
            <th>чт</th>
            <th>пт</th>
            <th>сб</th>
            <th>вс</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>
              <span class="date">27</span>
              <ul>
                <li v-for="thisrout in week1[0].rout" v-bind:key="thisrout.label">
                  <span> {{ thisrout.label }} </span>
                </li>
              </ul>
            </td>
            <td>
              <span class="date">28</span>
              <ul>
                <li v-for="thisrout in week1[1].rout" v-bind:class="[thisrout.label === ('Выходной' || 'Отпуск') ? 'orange-border' : 'green-border', thisrout.label === 'Офис' ? 'grey-border' : '' ]" v-bind:key="thisrout.label">
                  <span> {{ thisrout.label }} </span>
                </li>
              </ul>
            </td>
            <td>
              <span class="date">29</span>
              <ul>
                <li v-for="thisrout in week1[2].rout" v-bind:class="[thisrout.label === ('Выходной' || 'Отпуск') ? 'orange-border' : 'green-border', thisrout.label === 'Офис' ? 'grey-border' : '' ]" v-bind:key="thisrout.label">
                  <span> {{ thisrout.label }} </span>
                </li>
              </ul>
            </td>
            <td>
              <span class="date">30</span>
              <ul>
                <li v-for="thisrout in week1[3].rout" v-bind:class="[thisrout.label === ('Выходной' || 'Отпуск') ? 'orange-border' : 'green-border', thisrout.label === 'Офис' ? 'grey-border' : '' ]" v-bind:key="thisrout.label">
                  <span> {{ thisrout.label }} </span>
                </li>
              </ul>
            </td>
            <td>
              <span class="date">31</span>
              <ul>
                <li v-for="thisrout in week1[4].rout" v-bind:class="[thisrout.label === ('Выходной' || 'Отпуск') ? 'orange-border' : 'green-border', thisrout.label === 'Офис' ? 'grey-border' : '' ]" v-bind:key="thisrout.label">
                  <span> {{ thisrout.label }} </span>
                </li>
              </ul>
            </td>
            <td>
              <span class="date">1</span>
              <ul>
                <li v-for="thisrout in week1[5].rout" v-bind:class="[thisrout.label === ('Выходной' || 'Отпуск') ? 'orange-border' : 'green-border', thisrout.label === 'Офис' ? 'grey-border' : '' ]" v-bind:key="thisrout.label">
                  <span> {{ thisrout.label }} </span>
                </li>
              </ul>
            </td>
            <td>
              <span class="date">2</span>
              <ul>
                <li v-for="thisrout in week1[6].rout" v-bind:class="[thisrout.label === ('Выходной' || 'Отпуск') ? 'orange-border' : 'green-border', thisrout.label === 'Офис' ? 'grey-border' : '' ]" v-bind:key="thisrout.label">
                  <span> {{ thisrout.label }} </span>
                </li>
              </ul>
            </td>
          </tr>
          <tr>
            <td>
              <span class="date">3</span>
              <ul>
                <li v-for="thisrout in week2[0].rout" v-bind:class="[thisrout.label === ('Выходной' || 'Отпуск') ? 'orange-border' : 'green-border', thisrout.label === 'Офис' ? 'grey-border' : '' ]" v-bind:key="thisrout.label">
                  <span> {{ thisrout.label }} </span>
                </li>
              </ul>
            </td>
            <td>
              <span class="date">4</span>
              <ul>
                <li v-for="thisrout in week2[1].rout" v-bind:class="[thisrout.label === ('Выходной' || 'Отпуск') ? 'orange-border' : 'green-border', thisrout.label === 'Офис' ? 'grey-border' : '' ]" v-bind:key="thisrout.label">
                  <span> {{ thisrout.label }} </span>
                </li>
              </ul>
            </td>
            <td>
              <span class="date">5</span>
              <ul>
                <li v-for="thisrout in week2[2].rout" v-bind:class="[thisrout.label === ('Выходной' || 'Отпуск') ? 'orange-border' : 'green-border', thisrout.label === 'Офис' ? 'grey-border' : '' ]" v-bind:key="thisrout.label">
                  <span> {{ thisrout.label }} </span>
                </li>
              </ul>
            </td>
            <td>
              <span class="date">6</span>
              <ul>
                <li v-for="thisrout in week2[3].rout" v-bind:class="[thisrout.label === ('Выходной' || 'Отпуск') ? 'orange-border' : 'green-border', thisrout.label === 'Офис' ? 'grey-border' : '' ]" v-bind:key="thisrout.label">
                  <span> {{ thisrout.label }} </span>
                </li>
              </ul>
            </td>
            <td>
              <span class="date">7</span>
              <ul>
                <li v-for="thisrout in week2[4].rout" v-bind:class="[thisrout.label === ('Выходной' || 'Отпуск') ? 'orange-border' : 'green-border', thisrout.label === 'Офис' ? 'grey-border' : '' ]" v-bind:key="thisrout.label">
                  <span> {{ thisrout.label }} </span>
                </li>
              </ul>
            </td>
            <td>
              <span class="date">8</span>
              <ul>
                <li v-for="thisrout in week2[5].rout" v-bind:class="[thisrout.label === ('Выходной' || 'Отпуск') ? 'orange-border' : 'green-border', thisrout.label === 'Офис' ? 'grey-border' : '' ]" v-bind:key="thisrout.label">
                  <span> {{ thisrout.label }} </span>
                </li>
              </ul>
            </td>
            <td>
              <span class="date">9</span>
              <div>
              <ul>
                
                  <li v-for="thisrout in week2[6].rout" v-bind:class="[thisrout.label === ('Выходной' || 'Отпуск') ? 'orange-border' : 'green-border', thisrout.label === 'Офис' ? 'grey-border' : '' ]" v-bind:key="thisrout.label">
                  <span v-if="thisrout.id < 3"> {{ thisrout.label }} </span>
                </li>
                <li v-if="week2[6].rout.length > 3" class="all-routs"> <b-button id="popover-1" class="text-o" style="font-size: 12px; white-space: nowrap">все 12 маршрутов</b-button></li>
                <b-popover target="popover-1" triggers="hover focus">
                  <div class="left-popover-content">
                      <ul>
                        <li v-for="thisrout in week2[6].rout" v-bind:key="thisrout.label">
                            <span> {{ thisrout.label }} </span>
                        </li>
                      </ul>
                  </div>
                  <div class="right-popover-content">

                  </div>
                </b-popover>
              </ul>
              
                </div>
            </td>
          </tr>
          <tr>
            <td>
              <span class="date">10</span>
              <ul>
                <li v-for="thisrout in week3[0].rout" v-bind:class="[thisrout.label === ('Выходной' || 'Отпуск') ? 'orange-border' : 'green-border', thisrout.label === 'Офис' ? 'grey-border' : '' ]" v-bind:key="thisrout.label">
                  <span> {{ thisrout.label }} </span>
                </li>
              </ul>
            </td>
            <td>
              <span class="date">11</span>
              <ul>
                <li v-for="thisrout in week3[1].rout" v-bind:class="[thisrout.label === ('Выходной' || 'Отпуск') ? 'orange-border' : 'green-border', thisrout.label === 'Офис' ? 'grey-border' : '' ]" v-bind:key="thisrout.label">
                  <span> {{ thisrout.label }} </span>
                </li>
              </ul>
            </td>
            <td>
              <span class="date">12</span>
              <ul>
                <li v-for="thisrout in week3[2].rout" v-bind:class="[thisrout.label === ('Выходной' || 'Отпуск') ? 'orange-border' : 'green-border', thisrout.label === 'Офис' ? 'grey-border' : '' ]" v-bind:key="thisrout.label">
                  <span> {{ thisrout.label }} </span>
                </li>
              </ul>
            </td>
            <td>
              <span class="date">13</span>
              <ul>
                <li v-for="thisrout in week3[3].rout" v-bind:class="[thisrout.label === ('Выходной' || 'Отпуск') ? 'orange-border' : 'green-border', thisrout.label === 'Офис' ? 'grey-border' : '' ]" v-bind:key="thisrout.label">
                  <span> {{ thisrout.label }} </span>
                </li>
              </ul>
            </td>
            <td>
              <span class="date">14</span>
              <ul>
                <li v-for="thisrout in week3[4].rout" v-bind:class="[thisrout.label === ('Выходной' || 'Отпуск') ? 'orange-border' : 'green-border', thisrout.label === 'Офис' ? 'grey-border' : '' ]" v-bind:key="thisrout.label">
                  <span> {{ thisrout.label }} </span>
                </li>
              </ul>
            </td>
            <td>
              <span class="date">15</span>
              <ul>
                <li v-for="thisrout in week3[5].rout" v-bind:class="[thisrout.label === ('Выходной' || 'Отпуск') ? 'orange-border' : 'green-border', thisrout.label === 'Офис' ? 'grey-border' : '' ]" v-bind:key="thisrout.label">
                  <span> {{ thisrout.label }} </span>
                </li>
              </ul>
            </td>
            <td>
              <span class="date">16</span>
              <ul>
                <li v-for="thisrout in week3[6].rout" v-bind:class="[thisrout.label === ('Выходной' || 'Отпуск') ? 'orange-border' : 'green-border', thisrout.label === 'Офис' ? 'grey-border' : '' ]" v-bind:key="thisrout.label">
                  <span> {{ thisrout.label }} </span>
                </li>
              </ul>
            </td>
          </tr>
          <tr>
            <td>
              <span class="date">17</span>
              <ul>
                <li v-for="thisrout in week4[0].rout" v-bind:class="[thisrout.label === ('Выходной' || 'Отпуск') ? 'orange-border' : 'green-border', thisrout.label === 'Офис' ? 'grey-border' : '' ]" v-bind:key="thisrout.label">
                  <span> {{ thisrout.label }} </span>
                </li>
              </ul>
            </td>
            <td>
              <span class="date">18</span>
              <ul>
                <li v-for="thisrout in week4[1].rout" v-bind:class="[thisrout.label === ('Выходной' || 'Отпуск') ? 'orange-border' : 'green-border', thisrout.label === 'Офис' ? 'grey-border' : '' ]" v-bind:key="thisrout.label">
                  <span> {{ thisrout.label }} </span>
                </li>
              </ul>
            </td>
            <td>
              <span class="date">19</span>
              <ul>
                <li v-for="thisrout in week4[2].rout" v-bind:class="[thisrout.label === ('Выходной' || 'Отпуск') ? 'orange-border' : 'green-border', thisrout.label === 'Офис' ? 'grey-border' : '' ]" v-bind:key="thisrout.label">
                  <span> {{ thisrout.label }} </span>
                </li>
              </ul>
            </td>
            <td>
              <span class="date">20</span>
              <ul>
                <li v-for="thisrout in week4[3].rout" v-bind:class="[thisrout.label === ('Выходной' || 'Отпуск') ? 'orange-border' : 'green-border', thisrout.label === 'Офис' ? 'grey-border' : '' ]" v-bind:key="thisrout.label">
                  <span> {{ thisrout.label }} </span>
                </li>
              </ul>
            </td>
            <td>
              <span class="date">21</span>
              <ul>
                <li v-for="thisrout in week4[4].rout" v-bind:class="[thisrout.label === ('Выходной' || 'Отпуск') ? 'orange-border' : 'green-border', thisrout.label === 'Офис' ? 'grey-border' : '' ]" v-bind:key="thisrout.label">
                  <span> {{ thisrout.label }} </span>
                </li>
              </ul>
            </td>
            <td>
              <span class="date">22</span>
              <ul>
                <li v-for="thisrout in week4[5].rout" v-bind:class="[thisrout.label === ('Выходной' || 'Отпуск') ? 'orange-border' : 'green-border', thisrout.label === 'Офис' ? 'grey-border' : '' ]" v-bind:key="thisrout.label">
                  <span> {{ thisrout.label }} </span>
                </li>
              </ul>
            </td>
            <td>
              <span class="date">23</span>
              <ul>
                <li v-for="thisrout in week4[6].rout" v-bind:class="[thisrout.label === ('Выходной' || 'Отпуск') ? 'orange-border' : 'green-border', thisrout.label === 'Офис' ? 'grey-border' : '' ]" v-bind:key="thisrout.label">
                  <span> {{ thisrout.label }} </span>
                </li>
              </ul>
            </td>
          </tr>
          <tr>
            <td>
              <span class="date">24</span>
              <ul>
                <li v-for="thisrout in week5[0].rout" v-bind:class="[thisrout.label === ('Выходной' || 'Отпуск') ? 'orange-border' : 'green-border', thisrout.label === 'Офис' ? 'grey-border' : '' ]" v-bind:key="thisrout.label">
                  <span> {{ thisrout.label }} </span>
                </li>
              </ul>
            </td>
            <td>
              <span class="date">25</span>
              <ul>
                <li v-for="thisrout in week5[1].rout" v-bind:class="[thisrout.label === ('Выходной' || 'Отпуск') ? 'orange-border' : 'green-border', thisrout.label === 'Офис' ? 'grey-border' : '' ]" v-bind:key="thisrout.label">
                  <span> {{ thisrout.label }} </span>
                </li>
              </ul>
            </td>
            <td>
              <span class="date">26</span>
              <ul>
                <li v-for="thisrout in week5[2].rout" v-bind:class="[thisrout.label === ('Выходной' || 'Отпуск') ? 'orange-border' : 'green-border', thisrout.label === 'Офис' ? 'grey-border' : '' ]" v-bind:key="thisrout.label">
                  <span> {{ thisrout.label }} </span>
                </li>
              </ul>
            </td>
            <td>
              <span class="date">27</span>
              <ul>
                <li v-for="thisrout in week5[3].rout" v-bind:class="[thisrout.label === ('Выходной' || 'Отпуск') ? 'orange-border' : 'green-border', thisrout.label === 'Офис' ? 'grey-border' : '' ]" v-bind:key="thisrout.label">
                  <span> {{ thisrout.label }} </span>
                </li>
              </ul>
            </td>
            <td>
              <span class="date">28</span>
              <ul>
                <li v-for="thisrout in week5[4].rout" v-bind:class="[thisrout.label === ('Выходной' || 'Отпуск') ? 'orange-border' : 'green-border', thisrout.label === 'Офис' ? 'grey-border' : '' ]" v-bind:key="thisrout.label">
                  <span> {{ thisrout.label }} </span>
                </li>
              </ul>
            </td>
            <td>
              <span class="date">1</span>
              <ul>
                <li v-for="thisrout in week5[5].rout" v-bind:class="[thisrout.label === ('Выходной' || 'Отпуск') ? 'orange-border' : 'green-border', thisrout.label === 'Офис' ? 'grey-border' : '' ]" v-bind:key="thisrout.label">
                  <span> {{ thisrout.label }} </span>
                </li>
              </ul>
            </td>
            <td>
              <span class="date">2</span>
              <ul>
                <li v-for="thisrout in week5[6].rout" v-bind:class="[thisrout.label === ('Выходной' || 'Отпуск') ? 'orange-border' : 'green-border', thisrout.label === 'Офис' ? 'grey-border' : '' ]" v-bind:key="thisrout.label">
                  <span> {{ thisrout.label }} </span>
                </li>
              </ul>
            </td>
          </tr>
        </tbody>
      </table>
      </div>
      </div> 
    </div>
      
    <div class="right-content-wrap">
      <h1 class="right-content-header-text">Календарь</h1>
      <span class="calendar-header">Февраль</span>
      <table class="small-calendar">
        <thead>
          <tr>
            <th>пн</th>
            <th>вт</th>
            <th>ср</th>
            <th>чт</th>
            <th>пт</th>
            <th>сб</th>
            <th>вс</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td></td>
            <td></td>
            <td></td>
            <td>1</td>
            <td>2</td>
            <td>3</td>
            <td>4</td>
          </tr>
          <tr>
            <td>5</td>
            <td>6</td>
            <td>7</td>
            <td>8</td>
            <td>9</td>
            <td>10</td>
            <td>11</td>
          </tr>
          <tr>
            <td>12</td>
            <td>13</td>
            <td>14</td>
            <td>15</td>
            <td>16</td>
            <td>17</td>
            <td>18</td>
          </tr>
          <tr>
            <td>19</td>
            <td>20</td>
            <td>21</td>
            <td>22</td>
            <td>23</td>
            <td>24</td>
            <td>25</td>
          </tr>
          <tr>
            <td>26</td>
            <td>27</td>
            <td>28</td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
          </tr>
        </tbody>
      </table>
    </div>
    
    
    </div>
</b-container>
</div>
</template>

<script>
export default {
  name: "CalendarComponent",
  data() {
    return {

         week1 : [{value: 27, rout: []},
         {value: 28, rout: []},
         {value: 29, rout: []},
         {value: 30, rout: []},
         {value: 31, rout: []},
         {value: 1, rout: [{ id: 3, label: "Выходной", name: "", network: "", endTime: "", endDate: "", address: "" }]},
         {value: 2, rout: [{ id: 1, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}, 
         { id: 2, label: "Ашан-Сити-Орехово", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018", address: "143090, Краснознаменск, Молодежная д 2/1"},
         { id: 1, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}]}],

        week2 : [{value: 3, rout: [{ id: 1, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 2, label: "Ашан-Сити-Орехово", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018", address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 1, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 2, label: "Ашан-Сити-Орехово", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018", address: "143090, Краснознаменск, Молодежная д 2/1"}]},
        {value: 4, rout: [{ id: 4, label: "Офис", name: "", network: "", endTime: "", endDate: "", address: ""}]},
        {value: 5, rout: [{ id: 1, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 2, label: "Ашан-Сити-Орехово", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018", address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 1, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}]},
        {value: 6, rout: [{ id: 3, label: "Выходной", name: "", network: "", endTime: "", endDate: "", address: ""}]},
        {value: 7, rout: [{ id: 3, label: "Выходной", name: "", network: "", endTime: "", endDate: "", address: ""}]},
        {value: 8, rout: []},
        {value: 9, rout: [{ id: 1, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 2, label: "Ашан-Сити-Орехово", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018", address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 3, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 4, label: "Ашан-Сити-Орехово", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018", address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 5, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 6, label: "Ашан-Сити-Орехово", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018", address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 7, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 8, label: "Ашан-Сити-Орехово", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018", address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 9, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 10, label: "Ашан-Сити-Орехово", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018", address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 11, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 12, label: "Ашан-Сити-Орехово", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018", address: "143090, Краснознаменск, Молодежная д 2/1"}]}],

        week3: [{value: 10, rout: [{ id: 1, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 2, label: "Ашан-Сити-Орехово", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018", address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 1, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}]},
        {value: 11, rout: [{ id: 1, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 2, label: "Ашан-Сити-Орехово", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018", address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 1, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}]},
        {value: 12, rout: [{ id: 1, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 2, label: "Ашан-Сити-Орехово", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018", address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 1, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}]},
        {value: 13, rout: [{ id: 1, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 2, label: "Ашан-Сити-Орехово", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018", address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 1, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}]},
        {value: 14, rout: []},
        {value: 15, rout: [{ id: 1, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 2, label: "Ашан-Сити-Орехово", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018", address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 1, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}]},
        {value: 16, rout: [{ id: 1, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 2, label: "Ашан-Сити-Орехово", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018", address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 1, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}]}],

        week4: [{value: 17, rout: []},
        {value: 18, rout: []},
        {value: 19, rout: []},
        {value: 20, rout: []},
        {value: 21, rout: []},
        {value: 22, rout: []},
        {value: 23, rout: []}],

        week5: [{value: 24, rout: [{ id: 1, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 2, label: "Ашан-Сити-Орехово", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018", address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 1, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}]},
        {value: 25, rout: [{ id: 1, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 2, label: "Ашан-Сити-Орехово", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018", address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 1, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}]},
        {value: 26, rout: [{ id: 1, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 2, label: "Ашан-Сити-Орехово", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018", address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 1, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}]},
        {value: 27, rout: [{ id: 1, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 2, label: "Ашан-Сити-Орехово", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018", address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 1, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}]},
        {value: 28, rout: []},
        {value: 29, rout: [{ id: 1, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 2, label: "Ашан-Сити-Орехово", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018", address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 1, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}]},
        {value: 1, rout: [{ id: 1, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 2, label: "Ашан-Сити-Орехово", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018", address: "143090, Краснознаменск, Молодежная д 2/1"}, 
        { id: 1, label: "Чехов-Альттелеком", name: "205, МЮЗ, ОАО \"Моссковский Ювелирный завод\", г. Химки, Микрорайон Икея, корпус 2", network: "Белый ветер Цифровой", endTime: "14:27:15", endDate: "21.01.2018",address: "143090, Краснознаменск, Молодежная д 2/1"}]}],


    };
  },
  methods: {
    
  },
  created() {

  }
};
</script>

<style scoped>
 .navbar {
     background-color: #4a4a4a;
 }

 .badge {
    color: white;
    height: 17px;
    border-radius: 15px;
    background-color: green;
 }
 
 .settings {
   display: flex;
   flex-direction: row;
   justify-content: space-between;
 }

 .text-o, .text-o:hover, .btn-group > .btn, .btn-group > .btn :hover {
   color: black;
   background-color: white;
   border:none;
 }

 .breadcrumbs {
     margin-top: 30px;
     padding: 0 20px
 }

 .breadcrumbs-delimiter {
     margin: 0 15px;
 }

 .content {
   display: flex;
   flex-direction: row;
 }

 .left-content-wrap {
   flex-basis: 80%;
   padding: 0 20px;
 }

 .title-text {
   text-align: left;
 }

 .right-content-wrap {
   flex-basis: 20%;
   background-color: #f5f5f5;
   padding: 30px;
 }

 .right-content-header-text {
   text-align: left;
 }

 .small-calendar {
   width: 100%;
 }

.table th {
  border-top: none;
}

.table tr:last-child td {
  border-bottom: 1px solid #dee2e6;
}

 th {
   text-align: left
 }

 ul {
   padding: 0;
   margin-top: 10px;
 }

 li {
   list-style: none;
   margin-bottom: 5px;
 }

 li > span {
  font-size: 12px;
  font-family: "SourceSansPro";
  color: rgb(74, 74, 74);
  line-height: 1.667;
  margin-left: 10px;
  display: block;
  white-space: nowrap;
 }

 .all-routs {
   width:0;
   color: #52ae30;
 }

 .all-routs span {
   color: #52ae30;
 }

 .orange-border,
 .green-border,
 .grey-border {
  border-radius: 10px;
  margin-left: 2px;
  width: 5px;
  height: 100%;
 }

 .orange-border {
  background-color: rgb(255, 102, 0);
 }

 .green-border {
  background-color: #52ae30;
 }

 .grey-border {
  background-color: #4a4a4a;
 }



 .date {
  display: block;
  font-size: 16px;
  color: rgb(118, 118, 118);
  line-height: 1.25;
  text-align: left;
 }
</style>