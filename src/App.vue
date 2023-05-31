<template>
  <div class="card flex justify-content-center">
    <Dropdown
      v-model="selectedCity"
      editable
      :options="cities"
      optionLabel="city"
      placeholder="Select a City"
      class="w-full md:w-14rem"
      itemValue="city"
    />
  </div>
  <div class="card flex justify-content-center">
    <VCustomSelect
      v-model="selectedCity"
      :options="cities"
      label="city"
      placeholder="Select a City"
      class="w-full md:w-14rem"
    />
  </div>
  <div class="card flex justify-content-center">
    <va-select
      v-model="selectedCity"
      class="mb-6"
      label="track by"
      :options="cities"
      track-by="city"
      text-by="city"
    />
  </div>

  <div class="card flex justify-content-center">{{ selectedCity }}</div>
</template>

<script setup>
import { ref } from 'vue';

const selectedCity = ref({ city: 'Colchane', postalZip: 'EA97 6SD' });
const cities = ref([
  {
    city: 'Colchane',
    postalZip: 'EA97 6SD',
    cvv: 176,
  },
  {
    city: 'Queenstown',
    postalZip: '60410',
    cvv: 661,
  },
  {
    city: 'Chatillon',
    postalZip: '7504',
    cvv: 439,
  },
  {
    city: 'Chongqing',
    postalZip: '84-73',
    cvv: 122,
  },
  {
    city: 'Battagram',
    postalZip: '174827',
    cvv: 214,
  },
  {
    city: 'Bolsward',
    postalZip: '307237',
    cvv: 190,
  },
  {
    city: 'Kirriemuir',
    postalZip: '81-225',
    cvv: 487,
  },
  {
    city: 'Dera Ghazi Khan',
    postalZip: '297568',
    cvv: 864,
  },
  {
    city: 'Parauapebas',
    postalZip: '55330',
    cvv: 979,
  },
  {
    city: 'Makassar',
    postalZip: '46721',
    cvv: 497,
  },
  {
    city: 'Baubau',
    postalZip: '8144-4863',
    cvv: 556,
  },
  {
    city: 'Narvik',
    postalZip: '653035',
    cvv: 575,
  },
  {
    city: 'Inner Mongolia',
    postalZip: '15-37',
    cvv: 690,
  },
  {
    city: 'Arendal',
    postalZip: 'B43 1CX',
    cvv: 925,
  },
  {
    city: 'Kano',
    postalZip: '81447',
    cvv: 516,
  },
  {
    city: 'Koppervik',
    postalZip: '120258',
    cvv: 795,
  },
  {
    city: 'Boston',
    postalZip: '57635-56482',
    cvv: 862,
  },
  {
    city: 'Førde',
    postalZip: '62888',
    cvv: 891,
  },
  {
    city: 'Parauapebas',
    postalZip: '35947-59310',
    cvv: 644,
  },
  {
    city: 'Chuncheon',
    postalZip: '86571',
    cvv: 957,
  },
  {
    city: 'Juárez',
    postalZip: '597265',
    cvv: 769,
  },
  {
    city: 'Kano',
    postalZip: '25616-85776',
    cvv: 986,
  },
  {
    city: 'Malbaie',
    postalZip: '3854 MI',
    cvv: 953,
  },
  {
    city: 'Orchard',
    postalZip: '3138',
    cvv: 806,
  },
  {
    city: 'Chuncheon',
    postalZip: '6856-7564',
    cvv: 272,
  },
  {
    city: 'Tân An',
    postalZip: '97-32',
    cvv: 582,
  },
  {
    city: 'Elbistan',
    postalZip: '6267',
    cvv: 880,
  },
  {
    city: 'Valéncia',
    postalZip: '34117866',
    cvv: 144,
  },
  {
    city: 'Cockburn',
    postalZip: '73945',
    cvv: 364,
  },
  {
    city: 'Phalaborwa',
    postalZip: '6888',
    cvv: 492,
  },
  {
    city: 'Berwick',
    postalZip: '25-67',
    cvv: 629,
  },
  {
    city: 'Chihuahua',
    postalZip: '4308 EP',
    cvv: 298,
  },
  {
    city: 'Ninh Bình',
    postalZip: '4762 RT',
    cvv: 702,
  },
  {
    city: 'Sorsogon City',
    postalZip: '21175',
    cvv: 322,
  },
  {
    city: 'Tranås',
    postalZip: '6919',
    cvv: 689,
  },
  {
    city: 'Gdynia',
    postalZip: '866168',
    cvv: 311,
  },
  {
    city: 'Izmail',
    postalZip: '8055',
    cvv: 483,
  },
  {
    city: 'Potchefstroom',
    postalZip: '30703',
    cvv: 332,
  },
  {
    city: 'Pachuca',
    postalZip: '8283',
    cvv: 261,
  },
  {
    city: 'Zhejiang',
    postalZip: '6065',
    cvv: 920,
  },
  {
    city: 'Kallang',
    postalZip: '4523',
    cvv: 204,
  },
  {
    city: 'Bilbo',
    postalZip: '71663',
    cvv: 611,
  },
  {
    city: 'Oslo',
    postalZip: '93452-098',
    cvv: 469,
  },
  {
    city: 'Bastia',
    postalZip: '249247',
    cvv: 502,
  },
  {
    city: 'Lleida',
    postalZip: '32-41',
    cvv: 387,
  },
  {
    city: 'Chuncheon',
    postalZip: '298582',
    cvv: 747,
  },
  {
    city: 'Uddevalla',
    postalZip: '32749',
    cvv: 400,
  },
  {
    city: 'North-Eastern Islands',
    postalZip: 'WQ5I 1IK',
    cvv: 558,
  },
  {
    city: 'Odessa',
    postalZip: '7661',
    cvv: 984,
  },
  {
    city: 'Bắc Giang',
    postalZip: '958843',
    cvv: 602,
  },
  {
    city: 'Bukit Panjang',
    postalZip: '66853',
    cvv: 947,
  },
  {
    city: 'Manokwari',
    postalZip: '31361',
    cvv: 655,
  },
  {
    city: 'Dir',
    postalZip: '4774',
    cvv: 243,
  },
  {
    city: 'Selkirk',
    postalZip: '317445',
    cvv: 988,
  },
  {
    city: 'Kailua',
    postalZip: '7279',
    cvv: 292,
  },
  {
    city: 'Perchtoldsdorf',
    postalZip: '17489',
    cvv: 456,
  },
  {
    city: 'Vadsø',
    postalZip: '1345 YC',
    cvv: 988,
  },
  {
    city: 'Hebei',
    postalZip: '47182',
    cvv: 268,
  },
  {
    city: 'Celaya',
    postalZip: '432468',
    cvv: 534,
  },
  {
    city: 'Çermik',
    postalZip: '967769',
    cvv: 962,
  },
  {
    city: 'Nelspruit',
    postalZip: '41-34',
    cvv: 892,
  },
  {
    city: 'Cork',
    postalZip: '552435',
    cvv: 775,
  },
  {
    city: 'Torghar',
    postalZip: '11860',
    cvv: 652,
  },
  {
    city: 'Bischofshofen',
    postalZip: '20308',
    cvv: 549,
  },
  {
    city: 'Malaybalay',
    postalZip: '766027',
    cvv: 822,
  },
  {
    city: 'Goiânia',
    postalZip: '4271',
    cvv: 368,
  },
  {
    city: 'Thiaumont',
    postalZip: '863334',
    cvv: 735,
  },
  {
    city: 'Novena',
    postalZip: '42060',
    cvv: 688,
  },
  {
    city: 'Skien',
    postalZip: '2591 UE',
    cvv: 313,
  },
  {
    city: 'Rijkevorsel',
    postalZip: '7304',
    cvv: 462,
  },
  {
    city: 'Gävle',
    postalZip: '227986',
    cvv: 460,
  },
  {
    city: 'Gorontalo',
    postalZip: '249744',
    cvv: 222,
  },
  {
    city: 'Finspång',
    postalZip: '2291-0082',
    cvv: 220,
  },
  {
    city: 'Paya Lebar',
    postalZip: '273164',
    cvv: 858,
  },
  {
    city: 'Langesund',
    postalZip: '07257',
    cvv: 653,
  },
  {
    city: 'Ödemiş',
    postalZip: '41414',
    cvv: 377,
  },
  {
    city: 'Uitenhage',
    postalZip: '3622',
    cvv: 290,
  },
  {
    city: 'Port Harcourt',
    postalZip: '61512',
    cvv: 135,
  },
  {
    city: 'Bontang',
    postalZip: '40565',
    cvv: 266,
  },
  {
    city: 'Tocopilla',
    postalZip: '36918',
    cvv: 582,
  },
  {
    city: 'Hamburg',
    postalZip: '63-535',
    cvv: 684,
  },
  {
    city: 'Kaliningrad',
    postalZip: '6374 IP',
    cvv: 172,
  },
  {
    city: 'Palopo',
    postalZip: '13739',
    cvv: 126,
  },
  {
    city: 'Mödling',
    postalZip: '5554',
    cvv: 545,
  },
  {
    city: 'Anklam',
    postalZip: '361384',
    cvv: 363,
  },
  {
    city: 'San Jose',
    postalZip: '26741',
    cvv: 576,
  },
  {
    city: 'Białystok',
    postalZip: '9882',
    cvv: 232,
  },
  {
    city: 'Dublin',
    postalZip: '447798',
    cvv: 322,
  },
  {
    city: 'St. Neots',
    postalZip: 'X7W 6JE',
    cvv: 837,
  },
  {
    city: 'Bischofshofen',
    postalZip: '29497',
    cvv: 159,
  },
  {
    city: 'Ollagüe',
    postalZip: '1355',
    cvv: 867,
  },
  {
    city: 'Mataram',
    postalZip: 'Q1 2QB',
    cvv: 672,
  },
  {
    city: 'Førde',
    postalZip: '7661-2316',
    cvv: 474,
  },
  {
    city: 'Queenstown',
    postalZip: '745419',
    cvv: 258,
  },
  {
    city: 'Yogyakarta',
    postalZip: '002362',
    cvv: 585,
  },
  {
    city: 'Nasirabad',
    postalZip: 'Y8C 1H5',
    cvv: 406,
  },
  {
    city: 'Pamplona',
    postalZip: '80064',
    cvv: 154,
  },
  {
    city: 'Piła',
    postalZip: '64421',
    cvv: 878,
  },
  {
    city: 'Villahermosa',
    postalZip: '2475',
    cvv: 539,
  },
  {
    city: 'Vigo',
    postalZip: '7305',
    cvv: 914,
  },
  {
    city: 'Ashburton',
    postalZip: '816413',
    cvv: 941,
  },
  {
    city: 'Burnpur',
    postalZip: '44007',
    cvv: 619,
  },
  {
    city: 'Jiangsu',
    postalZip: '12715',
    cvv: 340,
  },
  {
    city: 'Seogwipo',
    postalZip: '54373-143',
    cvv: 677,
  },
  {
    city: 'Kano',
    postalZip: '05415',
    cvv: 683,
  },
  {
    city: 'Oordegem',
    postalZip: '73891',
    cvv: 123,
  },
  {
    city: 'Passi',
    postalZip: 'E58 9PV',
    cvv: 438,
  },
  {
    city: 'Dublin',
    postalZip: '04583',
    cvv: 275,
  },
  {
    city: 'Whitehorse',
    postalZip: '74941',
    cvv: 771,
  },
  {
    city: 'Tomaszów Mazowiecki',
    postalZip: '429211',
    cvv: 782,
  },
  {
    city: 'Macau',
    postalZip: '3773',
    cvv: 821,
  },
  {
    city: 'Mejillones',
    postalZip: '2853',
    cvv: 564,
  },
  {
    city: 'Flin Flon',
    postalZip: '7175',
    cvv: 708,
  },
  {
    city: 'Puntarenas',
    postalZip: '48759',
    cvv: 356,
  },
  {
    city: 'Pukekohe',
    postalZip: '181158',
    cvv: 146,
  },
  {
    city: 'Alta',
    postalZip: '555178',
    cvv: 844,
  },
  {
    city: 'Mokpo',
    postalZip: '30703',
    cvv: 419,
  },
  {
    city: 'Bekasi',
    postalZip: '19161',
    cvv: 352,
  },
  {
    city: 'Motala',
    postalZip: '9777 HC',
    cvv: 428,
  },
  {
    city: 'Vị Thanh',
    postalZip: '69463',
    cvv: 870,
  },
  {
    city: 'Rendsburg',
    postalZip: '234693',
    cvv: 618,
  },
  {
    city: 'Motala',
    postalZip: '756744',
    cvv: 344,
  },
  {
    city: 'Gangneung',
    postalZip: '2729',
    cvv: 643,
  },
  {
    city: 'Cauayan',
    postalZip: '25604-53279',
    cvv: 310,
  },
  {
    city: 'Upplands Väsby',
    postalZip: '7581 VH',
    cvv: 985,
  },
  {
    city: 'Bandung',
    postalZip: '2811 NH',
    cvv: 708,
  },
  {
    city: 'Crato',
    postalZip: '84162',
    cvv: 503,
  },
  {
    city: 'Leersum',
    postalZip: '386000',
    cvv: 321,
  },
  {
    city: 'Bajaur Agency',
    postalZip: '62663',
    cvv: 687,
  },
  {
    city: 'Rocky Mountain House',
    postalZip: '38-42',
    cvv: 432,
  },
  {
    city: 'Tuyên Quang',
    postalZip: '23470',
    cvv: 220,
  },
  {
    city: 'Bangalore',
    postalZip: '68948',
    cvv: 150,
  },
  {
    city: 'Mora',
    postalZip: '664832',
    cvv: 737,
  },
  {
    city: 'Villa del Rosario',
    postalZip: '305997',
    cvv: 860,
  },
  {
    city: 'Mitú',
    postalZip: '94684',
    cvv: 779,
  },
  {
    city: 'Nowshera',
    postalZip: '711212',
    cvv: 839,
  },
  {
    city: 'Canberra',
    postalZip: '8202',
    cvv: 642,
  },
  {
    city: 'Bristol',
    postalZip: '713559',
    cvv: 684,
  },
  {
    city: 'Emmen',
    postalZip: '4551',
    cvv: 829,
  },
  {
    city: 'Fundación',
    postalZip: '594351',
    cvv: 895,
  },
  {
    city: 'Whakatane',
    postalZip: '64572',
    cvv: 849,
  },
  {
    city: 'Völkermarkt',
    postalZip: '25545',
    cvv: 553,
  },
  {
    city: 'Invercargill',
    postalZip: '24495',
    cvv: 192,
  },
  {
    city: 'Stavoren',
    postalZip: '7163',
    cvv: 678,
  },
  {
    city: 'Erlangen',
    postalZip: '288167',
    cvv: 359,
  },
  {
    city: 'Palma de Mallorca',
    postalZip: '24-26',
    cvv: 647,
  },
  {
    city: 'Central Water Catchment',
    postalZip: '2384',
    cvv: 326,
  },
  {
    city: 'Vienna',
    postalZip: '566586',
    cvv: 963,
  },
  {
    city: 'Gore',
    postalZip: '82-35',
    cvv: 787,
  },
  {
    city: 'Winterswijk',
    postalZip: '689602',
    cvv: 625,
  },
  {
    city: 'Boryeong',
    postalZip: '75798',
    cvv: 648,
  },
  {
    city: 'Khyber Agency',
    postalZip: '349560',
    cvv: 526,
  },
  {
    city: 'Armidale',
    postalZip: '604821',
    cvv: 667,
  },
  {
    city: 'Kaneohe',
    postalZip: '05936',
    cvv: 506,
  },
  {
    city: 'Tumaco',
    postalZip: '50216',
    cvv: 150,
  },
  {
    city: 'Zaria',
    postalZip: '266258',
    cvv: 162,
  },
  {
    city: 'Nampa',
    postalZip: '71671',
    cvv: 522,
  },
  {
    city: 'Neustrelitz',
    postalZip: '30427',
    cvv: 802,
  },
  {
    city: 'Dagupan City',
    postalZip: '3904',
    cvv: 857,
  },
  {
    city: 'Dublin',
    postalZip: '7489 PX',
    cvv: 433,
  },
  {
    city: 'Belford Roxo',
    postalZip: '29137',
    cvv: 861,
  },
  {
    city: 'Glovertown',
    postalZip: '280571',
    cvv: 869,
  },
  {
    city: 'Kavaratti',
    postalZip: '04447',
    cvv: 267,
  },
  {
    city: 'Almere',
    postalZip: '50113',
    cvv: 441,
  },
  {
    city: 'Dublin',
    postalZip: '8569-9073',
    cvv: 593,
  },
  {
    city: 'Bama',
    postalZip: '392820',
    cvv: 990,
  },
  {
    city: 'Melilla',
    postalZip: '677888',
    cvv: 143,
  },
  {
    city: 'Nha Trang',
    postalZip: '645844',
    cvv: 369,
  },
  {
    city: 'Wrocław',
    postalZip: '68322',
    cvv: 915,
  },
  {
    city: 'Balıkesir',
    postalZip: '24562',
    cvv: 201,
  },
  {
    city: 'Großpetersdorf',
    postalZip: '6152',
    cvv: 843,
  },
  {
    city: 'Yeosu',
    postalZip: '265673',
    cvv: 425,
  },
  {
    city: 'Iquitos',
    postalZip: 'S1T 3L4',
    cvv: 527,
  },
  {
    city: 'Agartala',
    postalZip: '392503',
    cvv: 343,
  },
  {
    city: 'Voronezh',
    postalZip: '50407',
    cvv: 280,
  },
  {
    city: 'Lagos',
    postalZip: '96947',
    cvv: 921,
  },
  {
    city: 'Monterrey',
    postalZip: '293047',
    cvv: 477,
  },
  {
    city: 'Hunstanton',
    postalZip: '16428',
    cvv: 663,
  },
  {
    city: 'Peshawar',
    postalZip: '22-93',
    cvv: 396,
  },
  {
    city: 'Angoulême',
    postalZip: '13977',
    cvv: 810,
  },
  {
    city: 'Pievepelago',
    postalZip: '23515',
    cvv: 129,
  },
  {
    city: 'Pamplona',
    postalZip: '1716',
    cvv: 754,
  },
  {
    city: 'Dera Bugti',
    postalZip: '2106',
    cvv: 743,
  },
  {
    city: 'San Antonio',
    postalZip: '21648-117',
    cvv: 501,
  },
  {
    city: 'Tranås',
    postalZip: '2276-4347',
    cvv: 517,
  },
  {
    city: 'Rawalakot',
    postalZip: '511072',
    cvv: 779,
  },
  {
    city: 'Tauranga',
    postalZip: '25735',
    cvv: 846,
  },
  {
    city: 'Palma de Mallorca',
    postalZip: '627044',
    cvv: 611,
  },
  {
    city: 'Randburg',
    postalZip: '13-863',
    cvv: 534,
  },
  {
    city: 'Forres',
    postalZip: '26-33',
    cvv: 564,
  },
  {
    city: 'Mykolaiv',
    postalZip: '27869-80393',
    cvv: 586,
  },
  {
    city: 'Chortkiv',
    postalZip: '16685',
    cvv: 339,
  },
  {
    city: 'Brest',
    postalZip: '6430',
    cvv: 435,
  },
  {
    city: 'Voronezh',
    postalZip: '4136',
    cvv: 242,
  },
  {
    city: 'Hollabrunn',
    postalZip: '20418',
    cvv: 824,
  },
  {
    city: 'Vienna',
    postalZip: '358502',
    cvv: 465,
  },
  {
    city: 'Taupo',
    postalZip: '4406',
    cvv: 971,
  },
  {
    city: 'Narvik',
    postalZip: '4454',
    cvv: 138,
  },
  {
    city: 'Pinetown',
    postalZip: '7931',
    cvv: 669,
  },
  {
    city: 'Belfast',
    postalZip: '300617',
    cvv: 676,
  },
  {
    city: 'Batangas City',
    postalZip: 'HS22 7XO',
    cvv: 911,
  },
  {
    city: 'Cagnes-sur-Mer',
    postalZip: '538205',
    cvv: 168,
  },
  {
    city: 'Lerum',
    postalZip: '6233',
    cvv: 929,
  },
  {
    city: 'Berdychiv',
    postalZip: '6686 GF',
    cvv: 918,
  },
  {
    city: 'Monteu Roero',
    postalZip: '1921-3486',
    cvv: 274,
  },
  {
    city: 'Essex',
    postalZip: '59-145',
    cvv: 407,
  },
  {
    city: 'Whyalla',
    postalZip: 'A3N 8V9',
    cvv: 471,
  },
  {
    city: 'Yurimaguas',
    postalZip: '232820',
    cvv: 870,
  },
  {
    city: 'Hervey Bay',
    postalZip: '35414',
    cvv: 401,
  },
  {
    city: 'Götzis',
    postalZip: '58681-671',
    cvv: 310,
  },
  {
    city: 'Lipetsk',
    postalZip: '2644',
    cvv: 622,
  },
  {
    city: 'Yurimaguas',
    postalZip: '431517',
    cvv: 527,
  },
  {
    city: 'Dublin',
    postalZip: '3908',
    cvv: 997,
  },
  {
    city: 'Lochgilphead',
    postalZip: '86-61',
    cvv: 189,
  },
  {
    city: 'North-Eastern Islands',
    postalZip: '5827',
    cvv: 276,
  },
  {
    city: 'Tula',
    postalZip: '2171',
    cvv: 242,
  },
  {
    city: 'Skardu',
    postalZip: '3323 LJ',
    cvv: 312,
  },
  {
    city: 'Moulins',
    postalZip: '941673',
    cvv: 271,
  },
  {
    city: 'Cao Lãnh',
    postalZip: '73098',
    cvv: 250,
  },
  {
    city: 'Odessa',
    postalZip: '75822',
    cvv: 257,
  },
  {
    city: 'Great Yarmouth',
    postalZip: '7736',
    cvv: 694,
  },
  {
    city: 'Borlänge',
    postalZip: '438111',
    cvv: 291,
  },
  {
    city: 'Hồ Chí Minh City',
    postalZip: '03696',
    cvv: 736,
  },
  {
    city: 'Kediri',
    postalZip: '28-518',
    cvv: 437,
  },
  {
    city: 'Gravelbourg',
    postalZip: '722892',
    cvv: 706,
  },
  {
    city: 'Granada',
    postalZip: '84485',
    cvv: 772,
  },
  {
    city: 'Empangeni',
    postalZip: '68697',
    cvv: 310,
  },
  {
    city: 'Cabuyao',
    postalZip: '11665',
    cvv: 576,
  },
  {
    city: 'Pskov',
    postalZip: 'UI63 6KA',
    cvv: 435,
  },
  {
    city: 'Bhagalpur',
    postalZip: '67059-736',
    cvv: 235,
  },
  {
    city: 'Leticia',
    postalZip: '970623',
    cvv: 904,
  },
  {
    city: 'Denbigh',
    postalZip: '5822',
    cvv: 518,
  },
  {
    city: 'Mogi das Cruzes',
    postalZip: '18395',
    cvv: 809,
  },
  {
    city: 'Samsun',
    postalZip: '26796',
    cvv: 516,
  },
  {
    city: 'Kirov',
    postalZip: '23690',
    cvv: 584,
  },
  {
    city: 'Berdychiv',
    postalZip: '57186',
    cvv: 935,
  },
  {
    city: 'Cao Lãnh',
    postalZip: '58736',
    cvv: 294,
  },
  {
    city: 'Diego de Almagro',
    postalZip: '642159',
    cvv: 992,
  },
  {
    city: 'Paita',
    postalZip: '57-685',
    cvv: 968,
  },
  {
    city: 'Okara',
    postalZip: '63074',
    cvv: 917,
  },
  {
    city: "O'Higgins",
    postalZip: '6116-1320',
    cvv: 756,
  },
  {
    city: 'Frederick',
    postalZip: '582671',
    cvv: 672,
  },
  {
    city: 'Vadsø',
    postalZip: '927067',
    cvv: 411,
  },
  {
    city: 'Casper',
    postalZip: '64236',
    cvv: 332,
  },
  {
    city: 'Tyumen',
    postalZip: '42-28',
    cvv: 118,
  },
  {
    city: 'St. Pölten',
    postalZip: '142478',
    cvv: 201,
  },
  {
    city: 'Banjarmasin',
    postalZip: '5769-5275',
    cvv: 233,
  },
  {
    city: 'Blumenau',
    postalZip: '21282',
    cvv: 701,
  },
  {
    city: 'Chongqing',
    postalZip: 'A5Z 7E2',
    cvv: 407,
  },
  {
    city: 'Yemanzhelinsk',
    postalZip: 'T7R 2T6',
    cvv: 657,
  },
  {
    city: 'Huesca',
    postalZip: '4229',
    cvv: 152,
  },
  {
    city: 'Lutterworth',
    postalZip: 'UB9 9BF',
    cvv: 606,
  },
  {
    city: 'Lang',
    postalZip: '2752',
    cvv: 309,
  },
  {
    city: 'Tver',
    postalZip: '5608',
    cvv: 695,
  },
  {
    city: 'Kaliningrad',
    postalZip: '8112-5560',
    cvv: 491,
  },
  {
    city: 'Heilongjiang',
    postalZip: '83-591',
    cvv: 500,
  },
  {
    city: 'Namsos',
    postalZip: '25375-34722',
    cvv: 615,
  },
  {
    city: 'Cascavel',
    postalZip: '67M 5B2',
    cvv: 675,
  },
  {
    city: 'Paarl',
    postalZip: '16628',
    cvv: 155,
  },
  {
    city: 'Bragança',
    postalZip: '9273 CU',
    cvv: 891,
  },
  {
    city: 'Augusta',
    postalZip: '545673',
    cvv: 895,
  },
  {
    city: 'Cheltenham',
    postalZip: '829426',
    cvv: 694,
  },
  {
    city: 'Barranca',
    postalZip: '883846',
    cvv: 149,
  },
  {
    city: 'Blackwood',
    postalZip: '666476',
    cvv: 226,
  },
  {
    city: 'Olivar',
    postalZip: '18978',
    cvv: 941,
  },
  {
    city: 'Orito',
    postalZip: '48710',
    cvv: 145,
  },
  {
    city: 'Belém',
    postalZip: '4461',
    cvv: 717,
  },
  {
    city: 'Stevenage',
    postalZip: '5415',
    cvv: 701,
  },
  {
    city: 'Starachowice',
    postalZip: '212481',
    cvv: 619,
  },
  {
    city: 'Boise',
    postalZip: '66J 7N2',
    cvv: 493,
  },
  {
    city: 'Jiangsu',
    postalZip: '45697-72428',
    cvv: 198,
  },
  {
    city: 'Salamanca',
    postalZip: '68-83',
    cvv: 486,
  },
  {
    city: 'Hindeloopen',
    postalZip: '15125-390',
    cvv: 185,
  },
  {
    city: 'Dehradun',
    postalZip: '1788 MM',
    cvv: 597,
  },
  {
    city: 'Bragança',
    postalZip: '8723',
    cvv: 647,
  },
  {
    city: 'Port Moody',
    postalZip: '227241',
    cvv: 220,
  },
  {
    city: 'Aguazul',
    postalZip: '4045-4533',
    cvv: 187,
  },
  {
    city: 'Zapopan',
    postalZip: '546731',
    cvv: 960,
  },
  {
    city: 'Gressoney-La-Trinitè',
    postalZip: '16908-99104',
    cvv: 352,
  },
  {
    city: 'Petit-Hallet',
    postalZip: '414315',
    cvv: 312,
  },
  {
    city: 'Montigny-lès-Metz',
    postalZip: '91182-34235',
    cvv: 446,
  },
  {
    city: 'Alajuela',
    postalZip: '102516',
    cvv: 131,
  },
  {
    city: 'Cork',
    postalZip: '669455',
    cvv: 830,
  },
  {
    city: 'Liaoning',
    postalZip: '62791',
    cvv: 795,
  },
  {
    city: 'Lipa',
    postalZip: 'BH47 8SP',
    cvv: 440,
  },
  {
    city: 'Penza',
    postalZip: '54288',
    cvv: 828,
  },
  {
    city: 'Huelva',
    postalZip: '46215',
    cvv: 451,
  },
  {
    city: 'Szczecin',
    postalZip: '34528',
    cvv: 899,
  },
  {
    city: 'Montbliart',
    postalZip: '23837',
    cvv: 943,
  },
  {
    city: 'Cork',
    postalZip: '62796-325',
    cvv: 469,
  },
  {
    city: 'Port Augusta',
    postalZip: '42744',
    cvv: 388,
  },
  {
    city: 'Imphal',
    postalZip: '952399',
    cvv: 557,
  },
  {
    city: 'Kızılcahamam',
    postalZip: '54263',
    cvv: 482,
  },
  {
    city: 'Tierra Amarilla',
    postalZip: '78483',
    cvv: 383,
  },
  {
    city: 'Hangu',
    postalZip: '27761',
    cvv: 992,
  },
  {
    city: 'Tanjay',
    postalZip: '168531',
    cvv: 980,
  },
  {
    city: 'Tonalá',
    postalZip: '223064',
    cvv: 882,
  },
  {
    city: 'Fürstenwalde',
    postalZip: '78821',
    cvv: 306,
  },
  {
    city: 'Sapele',
    postalZip: '68461',
    cvv: 498,
  },
  {
    city: 'Bergama',
    postalZip: '5423',
    cvv: 702,
  },
  {
    city: 'Colchane',
    postalZip: 'EA97 6SD',
    cvv: 176,
  },
  {
    city: 'Queenstown',
    postalZip: '60410',
    cvv: 661,
  },
  {
    city: 'Chatillon',
    postalZip: '7504',
    cvv: 439,
  },
  {
    city: 'Chongqing',
    postalZip: '84-73',
    cvv: 122,
  },
  {
    city: 'Battagram',
    postalZip: '174827',
    cvv: 214,
  },
  {
    city: 'Bolsward',
    postalZip: '307237',
    cvv: 190,
  },
  {
    city: 'Kirriemuir',
    postalZip: '81-225',
    cvv: 487,
  },
  {
    city: 'Dera Ghazi Khan',
    postalZip: '297568',
    cvv: 864,
  },
  {
    city: 'Parauapebas',
    postalZip: '55330',
    cvv: 979,
  },
  {
    city: 'Makassar',
    postalZip: '46721',
    cvv: 497,
  },
  {
    city: 'Baubau',
    postalZip: '8144-4863',
    cvv: 556,
  },
  {
    city: 'Narvik',
    postalZip: '653035',
    cvv: 575,
  },
  {
    city: 'Inner Mongolia',
    postalZip: '15-37',
    cvv: 690,
  },
  {
    city: 'Arendal',
    postalZip: 'B43 1CX',
    cvv: 925,
  },
  {
    city: 'Kano',
    postalZip: '81447',
    cvv: 516,
  },
  {
    city: 'Koppervik',
    postalZip: '120258',
    cvv: 795,
  },
  {
    city: 'Boston',
    postalZip: '57635-56482',
    cvv: 862,
  },
  {
    city: 'Førde',
    postalZip: '62888',
    cvv: 891,
  },
  {
    city: 'Parauapebas',
    postalZip: '35947-59310',
    cvv: 644,
  },
  {
    city: 'Chuncheon',
    postalZip: '86571',
    cvv: 957,
  },
  {
    city: 'Juárez',
    postalZip: '597265',
    cvv: 769,
  },
  {
    city: 'Kano',
    postalZip: '25616-85776',
    cvv: 986,
  },
  {
    city: 'Malbaie',
    postalZip: '3854 MI',
    cvv: 953,
  },
  {
    city: 'Orchard',
    postalZip: '3138',
    cvv: 806,
  },
  {
    city: 'Chuncheon',
    postalZip: '6856-7564',
    cvv: 272,
  },
  {
    city: 'Tân An',
    postalZip: '97-32',
    cvv: 582,
  },
  {
    city: 'Elbistan',
    postalZip: '6267',
    cvv: 880,
  },
  {
    city: 'Valéncia',
    postalZip: '34117866',
    cvv: 144,
  },
  {
    city: 'Cockburn',
    postalZip: '73945',
    cvv: 364,
  },
  {
    city: 'Phalaborwa',
    postalZip: '6888',
    cvv: 492,
  },
  {
    city: 'Berwick',
    postalZip: '25-67',
    cvv: 629,
  },
  {
    city: 'Chihuahua',
    postalZip: '4308 EP',
    cvv: 298,
  },
  {
    city: 'Ninh Bình',
    postalZip: '4762 RT',
    cvv: 702,
  },
  {
    city: 'Sorsogon City',
    postalZip: '21175',
    cvv: 322,
  },
  {
    city: 'Tranås',
    postalZip: '6919',
    cvv: 689,
  },
  {
    city: 'Gdynia',
    postalZip: '866168',
    cvv: 311,
  },
  {
    city: 'Izmail',
    postalZip: '8055',
    cvv: 483,
  },
  {
    city: 'Potchefstroom',
    postalZip: '30703',
    cvv: 332,
  },
  {
    city: 'Pachuca',
    postalZip: '8283',
    cvv: 261,
  },
  {
    city: 'Zhejiang',
    postalZip: '6065',
    cvv: 920,
  },
  {
    city: 'Kallang',
    postalZip: '4523',
    cvv: 204,
  },
  {
    city: 'Bilbo',
    postalZip: '71663',
    cvv: 611,
  },
  {
    city: 'Oslo',
    postalZip: '93452-098',
    cvv: 469,
  },
  {
    city: 'Bastia',
    postalZip: '249247',
    cvv: 502,
  },
  {
    city: 'Lleida',
    postalZip: '32-41',
    cvv: 387,
  },
  {
    city: 'Chuncheon',
    postalZip: '298582',
    cvv: 747,
  },
  {
    city: 'Uddevalla',
    postalZip: '32749',
    cvv: 400,
  },
  {
    city: 'North-Eastern Islands',
    postalZip: 'WQ5I 1IK',
    cvv: 558,
  },
  {
    city: 'Odessa',
    postalZip: '7661',
    cvv: 984,
  },
  {
    city: 'Bắc Giang',
    postalZip: '958843',
    cvv: 602,
  },
  {
    city: 'Bukit Panjang',
    postalZip: '66853',
    cvv: 947,
  },
  {
    city: 'Manokwari',
    postalZip: '31361',
    cvv: 655,
  },
  {
    city: 'Dir',
    postalZip: '4774',
    cvv: 243,
  },
  {
    city: 'Selkirk',
    postalZip: '317445',
    cvv: 988,
  },
  {
    city: 'Kailua',
    postalZip: '7279',
    cvv: 292,
  },
  {
    city: 'Perchtoldsdorf',
    postalZip: '17489',
    cvv: 456,
  },
  {
    city: 'Vadsø',
    postalZip: '1345 YC',
    cvv: 988,
  },
  {
    city: 'Hebei',
    postalZip: '47182',
    cvv: 268,
  },
  {
    city: 'Celaya',
    postalZip: '432468',
    cvv: 534,
  },
  {
    city: 'Çermik',
    postalZip: '967769',
    cvv: 962,
  },
  {
    city: 'Nelspruit',
    postalZip: '41-34',
    cvv: 892,
  },
  {
    city: 'Cork',
    postalZip: '552435',
    cvv: 775,
  },
  {
    city: 'Torghar',
    postalZip: '11860',
    cvv: 652,
  },
  {
    city: 'Bischofshofen',
    postalZip: '20308',
    cvv: 549,
  },
  {
    city: 'Malaybalay',
    postalZip: '766027',
    cvv: 822,
  },
  {
    city: 'Goiânia',
    postalZip: '4271',
    cvv: 368,
  },
  {
    city: 'Thiaumont',
    postalZip: '863334',
    cvv: 735,
  },
  {
    city: 'Novena',
    postalZip: '42060',
    cvv: 688,
  },
  {
    city: 'Skien',
    postalZip: '2591 UE',
    cvv: 313,
  },
  {
    city: 'Rijkevorsel',
    postalZip: '7304',
    cvv: 462,
  },
  {
    city: 'Gävle',
    postalZip: '227986',
    cvv: 460,
  },
  {
    city: 'Gorontalo',
    postalZip: '249744',
    cvv: 222,
  },
  {
    city: 'Finspång',
    postalZip: '2291-0082',
    cvv: 220,
  },
  {
    city: 'Paya Lebar',
    postalZip: '273164',
    cvv: 858,
  },
  {
    city: 'Langesund',
    postalZip: '07257',
    cvv: 653,
  },
  {
    city: 'Ödemiş',
    postalZip: '41414',
    cvv: 377,
  },
  {
    city: 'Uitenhage',
    postalZip: '3622',
    cvv: 290,
  },
  {
    city: 'Port Harcourt',
    postalZip: '61512',
    cvv: 135,
  },
  {
    city: 'Bontang',
    postalZip: '40565',
    cvv: 266,
  },
  {
    city: 'Tocopilla',
    postalZip: '36918',
    cvv: 582,
  },
  {
    city: 'Hamburg',
    postalZip: '63-535',
    cvv: 684,
  },
  {
    city: 'Kaliningrad',
    postalZip: '6374 IP',
    cvv: 172,
  },
  {
    city: 'Palopo',
    postalZip: '13739',
    cvv: 126,
  },
  {
    city: 'Mödling',
    postalZip: '5554',
    cvv: 545,
  },
  {
    city: 'Anklam',
    postalZip: '361384',
    cvv: 363,
  },
  {
    city: 'San Jose',
    postalZip: '26741',
    cvv: 576,
  },
  {
    city: 'Białystok',
    postalZip: '9882',
    cvv: 232,
  },
  {
    city: 'Dublin',
    postalZip: '447798',
    cvv: 322,
  },
  {
    city: 'St. Neots',
    postalZip: 'X7W 6JE',
    cvv: 837,
  },
  {
    city: 'Bischofshofen',
    postalZip: '29497',
    cvv: 159,
  },
  {
    city: 'Ollagüe',
    postalZip: '1355',
    cvv: 867,
  },
  {
    city: 'Mataram',
    postalZip: 'Q1 2QB',
    cvv: 672,
  },
  {
    city: 'Førde',
    postalZip: '7661-2316',
    cvv: 474,
  },
  {
    city: 'Queenstown',
    postalZip: '745419',
    cvv: 258,
  },
  {
    city: 'Yogyakarta',
    postalZip: '002362',
    cvv: 585,
  },
  {
    city: 'Nasirabad',
    postalZip: 'Y8C 1H5',
    cvv: 406,
  },
  {
    city: 'Pamplona',
    postalZip: '80064',
    cvv: 154,
  },
  {
    city: 'Piła',
    postalZip: '64421',
    cvv: 878,
  },
  {
    city: 'Villahermosa',
    postalZip: '2475',
    cvv: 539,
  },
  {
    city: 'Vigo',
    postalZip: '7305',
    cvv: 914,
  },
  {
    city: 'Ashburton',
    postalZip: '816413',
    cvv: 941,
  },
  {
    city: 'Burnpur',
    postalZip: '44007',
    cvv: 619,
  },
  {
    city: 'Jiangsu',
    postalZip: '12715',
    cvv: 340,
  },
  {
    city: 'Seogwipo',
    postalZip: '54373-143',
    cvv: 677,
  },
  {
    city: 'Kano',
    postalZip: '05415',
    cvv: 683,
  },
  {
    city: 'Oordegem',
    postalZip: '73891',
    cvv: 123,
  },
  {
    city: 'Passi',
    postalZip: 'E58 9PV',
    cvv: 438,
  },
  {
    city: 'Dublin',
    postalZip: '04583',
    cvv: 275,
  },
  {
    city: 'Whitehorse',
    postalZip: '74941',
    cvv: 771,
  },
  {
    city: 'Tomaszów Mazowiecki',
    postalZip: '429211',
    cvv: 782,
  },
  {
    city: 'Macau',
    postalZip: '3773',
    cvv: 821,
  },
  {
    city: 'Mejillones',
    postalZip: '2853',
    cvv: 564,
  },
  {
    city: 'Flin Flon',
    postalZip: '7175',
    cvv: 708,
  },
  {
    city: 'Puntarenas',
    postalZip: '48759',
    cvv: 356,
  },
  {
    city: 'Pukekohe',
    postalZip: '181158',
    cvv: 146,
  },
  {
    city: 'Alta',
    postalZip: '555178',
    cvv: 844,
  },
  {
    city: 'Mokpo',
    postalZip: '30703',
    cvv: 419,
  },
  {
    city: 'Bekasi',
    postalZip: '19161',
    cvv: 352,
  },
  {
    city: 'Motala',
    postalZip: '9777 HC',
    cvv: 428,
  },
  {
    city: 'Vị Thanh',
    postalZip: '69463',
    cvv: 870,
  },
  {
    city: 'Rendsburg',
    postalZip: '234693',
    cvv: 618,
  },
  {
    city: 'Motala',
    postalZip: '756744',
    cvv: 344,
  },
  {
    city: 'Gangneung',
    postalZip: '2729',
    cvv: 643,
  },
  {
    city: 'Cauayan',
    postalZip: '25604-53279',
    cvv: 310,
  },
  {
    city: 'Upplands Väsby',
    postalZip: '7581 VH',
    cvv: 985,
  },
  {
    city: 'Bandung',
    postalZip: '2811 NH',
    cvv: 708,
  },
  {
    city: 'Crato',
    postalZip: '84162',
    cvv: 503,
  },
  {
    city: 'Leersum',
    postalZip: '386000',
    cvv: 321,
  },
  {
    city: 'Bajaur Agency',
    postalZip: '62663',
    cvv: 687,
  },
  {
    city: 'Rocky Mountain House',
    postalZip: '38-42',
    cvv: 432,
  },
  {
    city: 'Tuyên Quang',
    postalZip: '23470',
    cvv: 220,
  },
  {
    city: 'Bangalore',
    postalZip: '68948',
    cvv: 150,
  },
  {
    city: 'Mora',
    postalZip: '664832',
    cvv: 737,
  },
  {
    city: 'Villa del Rosario',
    postalZip: '305997',
    cvv: 860,
  },
  {
    city: 'Mitú',
    postalZip: '94684',
    cvv: 779,
  },
  {
    city: 'Nowshera',
    postalZip: '711212',
    cvv: 839,
  },
  {
    city: 'Canberra',
    postalZip: '8202',
    cvv: 642,
  },
  {
    city: 'Bristol',
    postalZip: '713559',
    cvv: 684,
  },
  {
    city: 'Emmen',
    postalZip: '4551',
    cvv: 829,
  },
  {
    city: 'Fundación',
    postalZip: '594351',
    cvv: 895,
  },
  {
    city: 'Whakatane',
    postalZip: '64572',
    cvv: 849,
  },
  {
    city: 'Völkermarkt',
    postalZip: '25545',
    cvv: 553,
  },
  {
    city: 'Invercargill',
    postalZip: '24495',
    cvv: 192,
  },
  {
    city: 'Stavoren',
    postalZip: '7163',
    cvv: 678,
  },
  {
    city: 'Erlangen',
    postalZip: '288167',
    cvv: 359,
  },
  {
    city: 'Palma de Mallorca',
    postalZip: '24-26',
    cvv: 647,
  },
  {
    city: 'Central Water Catchment',
    postalZip: '2384',
    cvv: 326,
  },
  {
    city: 'Vienna',
    postalZip: '566586',
    cvv: 963,
  },
  {
    city: 'Gore',
    postalZip: '82-35',
    cvv: 787,
  },
  {
    city: 'Winterswijk',
    postalZip: '689602',
    cvv: 625,
  },
  {
    city: 'Boryeong',
    postalZip: '75798',
    cvv: 648,
  },
  {
    city: 'Khyber Agency',
    postalZip: '349560',
    cvv: 526,
  },
  {
    city: 'Armidale',
    postalZip: '604821',
    cvv: 667,
  },
  {
    city: 'Kaneohe',
    postalZip: '05936',
    cvv: 506,
  },
  {
    city: 'Tumaco',
    postalZip: '50216',
    cvv: 150,
  },
  {
    city: 'Zaria',
    postalZip: '266258',
    cvv: 162,
  },
  {
    city: 'Nampa',
    postalZip: '71671',
    cvv: 522,
  },
  {
    city: 'Neustrelitz',
    postalZip: '30427',
    cvv: 802,
  },
  {
    city: 'Dagupan City',
    postalZip: '3904',
    cvv: 857,
  },
  {
    city: 'Dublin',
    postalZip: '7489 PX',
    cvv: 433,
  },
  {
    city: 'Belford Roxo',
    postalZip: '29137',
    cvv: 861,
  },
  {
    city: 'Glovertown',
    postalZip: '280571',
    cvv: 869,
  },
  {
    city: 'Kavaratti',
    postalZip: '04447',
    cvv: 267,
  },
  {
    city: 'Almere',
    postalZip: '50113',
    cvv: 441,
  },
  {
    city: 'Dublin',
    postalZip: '8569-9073',
    cvv: 593,
  },
  {
    city: 'Bama',
    postalZip: '392820',
    cvv: 990,
  },
  {
    city: 'Melilla',
    postalZip: '677888',
    cvv: 143,
  },
  {
    city: 'Nha Trang',
    postalZip: '645844',
    cvv: 369,
  },
  {
    city: 'Wrocław',
    postalZip: '68322',
    cvv: 915,
  },
  {
    city: 'Balıkesir',
    postalZip: '24562',
    cvv: 201,
  },
  {
    city: 'Großpetersdorf',
    postalZip: '6152',
    cvv: 843,
  },
  {
    city: 'Yeosu',
    postalZip: '265673',
    cvv: 425,
  },
  {
    city: 'Iquitos',
    postalZip: 'S1T 3L4',
    cvv: 527,
  },
  {
    city: 'Agartala',
    postalZip: '392503',
    cvv: 343,
  },
  {
    city: 'Voronezh',
    postalZip: '50407',
    cvv: 280,
  },
  {
    city: 'Lagos',
    postalZip: '96947',
    cvv: 921,
  },
  {
    city: 'Monterrey',
    postalZip: '293047',
    cvv: 477,
  },
  {
    city: 'Hunstanton',
    postalZip: '16428',
    cvv: 663,
  },
  {
    city: 'Peshawar',
    postalZip: '22-93',
    cvv: 396,
  },
  {
    city: 'Angoulême',
    postalZip: '13977',
    cvv: 810,
  },
  {
    city: 'Pievepelago',
    postalZip: '23515',
    cvv: 129,
  },
  {
    city: 'Pamplona',
    postalZip: '1716',
    cvv: 754,
  },
  {
    city: 'Dera Bugti',
    postalZip: '2106',
    cvv: 743,
  },
  {
    city: 'San Antonio',
    postalZip: '21648-117',
    cvv: 501,
  },
  {
    city: 'Tranås',
    postalZip: '2276-4347',
    cvv: 517,
  },
  {
    city: 'Rawalakot',
    postalZip: '511072',
    cvv: 779,
  },
  {
    city: 'Tauranga',
    postalZip: '25735',
    cvv: 846,
  },
  {
    city: 'Palma de Mallorca',
    postalZip: '627044',
    cvv: 611,
  },
  {
    city: 'Randburg',
    postalZip: '13-863',
    cvv: 534,
  },
  {
    city: 'Forres',
    postalZip: '26-33',
    cvv: 564,
  },
  {
    city: 'Mykolaiv',
    postalZip: '27869-80393',
    cvv: 586,
  },
  {
    city: 'Chortkiv',
    postalZip: '16685',
    cvv: 339,
  },
  {
    city: 'Brest',
    postalZip: '6430',
    cvv: 435,
  },
  {
    city: 'Voronezh',
    postalZip: '4136',
    cvv: 242,
  },
  {
    city: 'Hollabrunn',
    postalZip: '20418',
    cvv: 824,
  },
  {
    city: 'Vienna',
    postalZip: '358502',
    cvv: 465,
  },
  {
    city: 'Taupo',
    postalZip: '4406',
    cvv: 971,
  },
  {
    city: 'Narvik',
    postalZip: '4454',
    cvv: 138,
  },
  {
    city: 'Pinetown',
    postalZip: '7931',
    cvv: 669,
  },
  {
    city: 'Belfast',
    postalZip: '300617',
    cvv: 676,
  },
  {
    city: 'Batangas City',
    postalZip: 'HS22 7XO',
    cvv: 911,
  },
  {
    city: 'Cagnes-sur-Mer',
    postalZip: '538205',
    cvv: 168,
  },
  {
    city: 'Lerum',
    postalZip: '6233',
    cvv: 929,
  },
  {
    city: 'Berdychiv',
    postalZip: '6686 GF',
    cvv: 918,
  },
  {
    city: 'Monteu Roero',
    postalZip: '1921-3486',
    cvv: 274,
  },
  {
    city: 'Essex',
    postalZip: '59-145',
    cvv: 407,
  },
  {
    city: 'Whyalla',
    postalZip: 'A3N 8V9',
    cvv: 471,
  },
  {
    city: 'Yurimaguas',
    postalZip: '232820',
    cvv: 870,
  },
  {
    city: 'Hervey Bay',
    postalZip: '35414',
    cvv: 401,
  },
  {
    city: 'Götzis',
    postalZip: '58681-671',
    cvv: 310,
  },
  {
    city: 'Lipetsk',
    postalZip: '2644',
    cvv: 622,
  },
  {
    city: 'Yurimaguas',
    postalZip: '431517',
    cvv: 527,
  },
  {
    city: 'Dublin',
    postalZip: '3908',
    cvv: 997,
  },
  {
    city: 'Lochgilphead',
    postalZip: '86-61',
    cvv: 189,
  },
  {
    city: 'North-Eastern Islands',
    postalZip: '5827',
    cvv: 276,
  },
  {
    city: 'Tula',
    postalZip: '2171',
    cvv: 242,
  },
  {
    city: 'Skardu',
    postalZip: '3323 LJ',
    cvv: 312,
  },
  {
    city: 'Moulins',
    postalZip: '941673',
    cvv: 271,
  },
  {
    city: 'Cao Lãnh',
    postalZip: '73098',
    cvv: 250,
  },
  {
    city: 'Odessa',
    postalZip: '75822',
    cvv: 257,
  },
  {
    city: 'Great Yarmouth',
    postalZip: '7736',
    cvv: 694,
  },
  {
    city: 'Borlänge',
    postalZip: '438111',
    cvv: 291,
  },
  {
    city: 'Hồ Chí Minh City',
    postalZip: '03696',
    cvv: 736,
  },
  {
    city: 'Kediri',
    postalZip: '28-518',
    cvv: 437,
  },
  {
    city: 'Gravelbourg',
    postalZip: '722892',
    cvv: 706,
  },
  {
    city: 'Granada',
    postalZip: '84485',
    cvv: 772,
  },
  {
    city: 'Empangeni',
    postalZip: '68697',
    cvv: 310,
  },
  {
    city: 'Cabuyao',
    postalZip: '11665',
    cvv: 576,
  },
  {
    city: 'Pskov',
    postalZip: 'UI63 6KA',
    cvv: 435,
  },
  {
    city: 'Bhagalpur',
    postalZip: '67059-736',
    cvv: 235,
  },
  {
    city: 'Leticia',
    postalZip: '970623',
    cvv: 904,
  },
  {
    city: 'Denbigh',
    postalZip: '5822',
    cvv: 518,
  },
  {
    city: 'Mogi das Cruzes',
    postalZip: '18395',
    cvv: 809,
  },
  {
    city: 'Samsun',
    postalZip: '26796',
    cvv: 516,
  },
  {
    city: 'Kirov',
    postalZip: '23690',
    cvv: 584,
  },
  {
    city: 'Berdychiv',
    postalZip: '57186',
    cvv: 935,
  },
  {
    city: 'Cao Lãnh',
    postalZip: '58736',
    cvv: 294,
  },
  {
    city: 'Diego de Almagro',
    postalZip: '642159',
    cvv: 992,
  },
  {
    city: 'Paita',
    postalZip: '57-685',
    cvv: 968,
  },
  {
    city: 'Okara',
    postalZip: '63074',
    cvv: 917,
  },
  {
    city: "O'Higgins",
    postalZip: '6116-1320',
    cvv: 756,
  },
  {
    city: 'Frederick',
    postalZip: '582671',
    cvv: 672,
  },
  {
    city: 'Vadsø',
    postalZip: '927067',
    cvv: 411,
  },
  {
    city: 'Casper',
    postalZip: '64236',
    cvv: 332,
  },
  {
    city: 'Tyumen',
    postalZip: '42-28',
    cvv: 118,
  },
  {
    city: 'St. Pölten',
    postalZip: '142478',
    cvv: 201,
  },
  {
    city: 'Banjarmasin',
    postalZip: '5769-5275',
    cvv: 233,
  },
  {
    city: 'Blumenau',
    postalZip: '21282',
    cvv: 701,
  },
  {
    city: 'Chongqing',
    postalZip: 'A5Z 7E2',
    cvv: 407,
  },
  {
    city: 'Yemanzhelinsk',
    postalZip: 'T7R 2T6',
    cvv: 657,
  },
  {
    city: 'Huesca',
    postalZip: '4229',
    cvv: 152,
  },
  {
    city: 'Lutterworth',
    postalZip: 'UB9 9BF',
    cvv: 606,
  },
  {
    city: 'Lang',
    postalZip: '2752',
    cvv: 309,
  },
  {
    city: 'Tver',
    postalZip: '5608',
    cvv: 695,
  },
  {
    city: 'Kaliningrad',
    postalZip: '8112-5560',
    cvv: 491,
  },
  {
    city: 'Heilongjiang',
    postalZip: '83-591',
    cvv: 500,
  },
  {
    city: 'Namsos',
    postalZip: '25375-34722',
    cvv: 615,
  },
  {
    city: 'Cascavel',
    postalZip: '67M 5B2',
    cvv: 675,
  },
  {
    city: 'Paarl',
    postalZip: '16628',
    cvv: 155,
  },
  {
    city: 'Bragança',
    postalZip: '9273 CU',
    cvv: 891,
  },
  {
    city: 'Augusta',
    postalZip: '545673',
    cvv: 895,
  },
  {
    city: 'Cheltenham',
    postalZip: '829426',
    cvv: 694,
  },
  {
    city: 'Barranca',
    postalZip: '883846',
    cvv: 149,
  },
  {
    city: 'Blackwood',
    postalZip: '666476',
    cvv: 226,
  },
  {
    city: 'Olivar',
    postalZip: '18978',
    cvv: 941,
  },
  {
    city: 'Orito',
    postalZip: '48710',
    cvv: 145,
  },
  {
    city: 'Belém',
    postalZip: '4461',
    cvv: 717,
  },
  {
    city: 'Stevenage',
    postalZip: '5415',
    cvv: 701,
  },
  {
    city: 'Starachowice',
    postalZip: '212481',
    cvv: 619,
  },
  {
    city: 'Boise',
    postalZip: '66J 7N2',
    cvv: 493,
  },
  {
    city: 'Jiangsu',
    postalZip: '45697-72428',
    cvv: 198,
  },
  {
    city: 'Salamanca',
    postalZip: '68-83',
    cvv: 486,
  },
  {
    city: 'Hindeloopen',
    postalZip: '15125-390',
    cvv: 185,
  },
  {
    city: 'Dehradun',
    postalZip: '1788 MM',
    cvv: 597,
  },
  {
    city: 'Bragança',
    postalZip: '8723',
    cvv: 647,
  },
  {
    city: 'Port Moody',
    postalZip: '227241',
    cvv: 220,
  },
  {
    city: 'Aguazul',
    postalZip: '4045-4533',
    cvv: 187,
  },
  {
    city: 'Zapopan',
    postalZip: '546731',
    cvv: 960,
  },
  {
    city: 'Gressoney-La-Trinitè',
    postalZip: '16908-99104',
    cvv: 352,
  },
  {
    city: 'Petit-Hallet',
    postalZip: '414315',
    cvv: 312,
  },
  {
    city: 'Montigny-lès-Metz',
    postalZip: '91182-34235',
    cvv: 446,
  },
  {
    city: 'Alajuela',
    postalZip: '102516',
    cvv: 131,
  },
  {
    city: 'Cork',
    postalZip: '669455',
    cvv: 830,
  },
  {
    city: 'Liaoning',
    postalZip: '62791',
    cvv: 795,
  },
  {
    city: 'Lipa',
    postalZip: 'BH47 8SP',
    cvv: 440,
  },
  {
    city: 'Penza',
    postalZip: '54288',
    cvv: 828,
  },
  {
    city: 'Huelva',
    postalZip: '46215',
    cvv: 451,
  },
  {
    city: 'Szczecin',
    postalZip: '34528',
    cvv: 899,
  },
  {
    city: 'Montbliart',
    postalZip: '23837',
    cvv: 943,
  },
  {
    city: 'Cork',
    postalZip: '62796-325',
    cvv: 469,
  },
  {
    city: 'Port Augusta',
    postalZip: '42744',
    cvv: 388,
  },
  {
    city: 'Imphal',
    postalZip: '952399',
    cvv: 557,
  },
  {
    city: 'Kızılcahamam',
    postalZip: '54263',
    cvv: 482,
  },
  {
    city: 'Tierra Amarilla',
    postalZip: '78483',
    cvv: 383,
  },
  {
    city: 'Hangu',
    postalZip: '27761',
    cvv: 992,
  },
  {
    city: 'Tanjay',
    postalZip: '168531',
    cvv: 980,
  },
  {
    city: 'Tonalá',
    postalZip: '223064',
    cvv: 882,
  },
  {
    city: 'Fürstenwalde',
    postalZip: '78821',
    cvv: 306,
  },
  {
    city: 'Sapele',
    postalZip: '68461',
    cvv: 498,
  },
  {
    city: 'Bergama',
    postalZip: '5423',
    cvv: 702,
  },
  {
    city: 'Colchane',
    postalZip: 'EA97 6SD',
    cvv: 176,
  },
  {
    city: 'Queenstown',
    postalZip: '60410',
    cvv: 661,
  },
  {
    city: 'Chatillon',
    postalZip: '7504',
    cvv: 439,
  },
  {
    city: 'Chongqing',
    postalZip: '84-73',
    cvv: 122,
  },
  {
    city: 'Battagram',
    postalZip: '174827',
    cvv: 214,
  },
  {
    city: 'Bolsward',
    postalZip: '307237',
    cvv: 190,
  },
  {
    city: 'Kirriemuir',
    postalZip: '81-225',
    cvv: 487,
  },
  {
    city: 'Dera Ghazi Khan',
    postalZip: '297568',
    cvv: 864,
  },
  {
    city: 'Parauapebas',
    postalZip: '55330',
    cvv: 979,
  },
  {
    city: 'Makassar',
    postalZip: '46721',
    cvv: 497,
  },
  {
    city: 'Baubau',
    postalZip: '8144-4863',
    cvv: 556,
  },
  {
    city: 'Narvik',
    postalZip: '653035',
    cvv: 575,
  },
  {
    city: 'Inner Mongolia',
    postalZip: '15-37',
    cvv: 690,
  },
  {
    city: 'Arendal',
    postalZip: 'B43 1CX',
    cvv: 925,
  },
  {
    city: 'Kano',
    postalZip: '81447',
    cvv: 516,
  },
  {
    city: 'Koppervik',
    postalZip: '120258',
    cvv: 795,
  },
  {
    city: 'Boston',
    postalZip: '57635-56482',
    cvv: 862,
  },
  {
    city: 'Førde',
    postalZip: '62888',
    cvv: 891,
  },
  {
    city: 'Parauapebas',
    postalZip: '35947-59310',
    cvv: 644,
  },
  {
    city: 'Chuncheon',
    postalZip: '86571',
    cvv: 957,
  },
  {
    city: 'Juárez',
    postalZip: '597265',
    cvv: 769,
  },
  {
    city: 'Kano',
    postalZip: '25616-85776',
    cvv: 986,
  },
  {
    city: 'Malbaie',
    postalZip: '3854 MI',
    cvv: 953,
  },
  {
    city: 'Orchard',
    postalZip: '3138',
    cvv: 806,
  },
  {
    city: 'Chuncheon',
    postalZip: '6856-7564',
    cvv: 272,
  },
  {
    city: 'Tân An',
    postalZip: '97-32',
    cvv: 582,
  },
  {
    city: 'Elbistan',
    postalZip: '6267',
    cvv: 880,
  },
  {
    city: 'Valéncia',
    postalZip: '34117866',
    cvv: 144,
  },
  {
    city: 'Cockburn',
    postalZip: '73945',
    cvv: 364,
  },
  {
    city: 'Phalaborwa',
    postalZip: '6888',
    cvv: 492,
  },
  {
    city: 'Berwick',
    postalZip: '25-67',
    cvv: 629,
  },
  {
    city: 'Chihuahua',
    postalZip: '4308 EP',
    cvv: 298,
  },
  {
    city: 'Ninh Bình',
    postalZip: '4762 RT',
    cvv: 702,
  },
  {
    city: 'Sorsogon City',
    postalZip: '21175',
    cvv: 322,
  },
  {
    city: 'Tranås',
    postalZip: '6919',
    cvv: 689,
  },
  {
    city: 'Gdynia',
    postalZip: '866168',
    cvv: 311,
  },
  {
    city: 'Izmail',
    postalZip: '8055',
    cvv: 483,
  },
  {
    city: 'Potchefstroom',
    postalZip: '30703',
    cvv: 332,
  },
  {
    city: 'Pachuca',
    postalZip: '8283',
    cvv: 261,
  },
  {
    city: 'Zhejiang',
    postalZip: '6065',
    cvv: 920,
  },
  {
    city: 'Kallang',
    postalZip: '4523',
    cvv: 204,
  },
  {
    city: 'Bilbo',
    postalZip: '71663',
    cvv: 611,
  },
  {
    city: 'Oslo',
    postalZip: '93452-098',
    cvv: 469,
  },
  {
    city: 'Bastia',
    postalZip: '249247',
    cvv: 502,
  },
  {
    city: 'Lleida',
    postalZip: '32-41',
    cvv: 387,
  },
  {
    city: 'Chuncheon',
    postalZip: '298582',
    cvv: 747,
  },
  {
    city: 'Uddevalla',
    postalZip: '32749',
    cvv: 400,
  },
  {
    city: 'North-Eastern Islands',
    postalZip: 'WQ5I 1IK',
    cvv: 558,
  },
  {
    city: 'Odessa',
    postalZip: '7661',
    cvv: 984,
  },
  {
    city: 'Bắc Giang',
    postalZip: '958843',
    cvv: 602,
  },
  {
    city: 'Bukit Panjang',
    postalZip: '66853',
    cvv: 947,
  },
  {
    city: 'Manokwari',
    postalZip: '31361',
    cvv: 655,
  },
  {
    city: 'Dir',
    postalZip: '4774',
    cvv: 243,
  },
  {
    city: 'Selkirk',
    postalZip: '317445',
    cvv: 988,
  },
  {
    city: 'Kailua',
    postalZip: '7279',
    cvv: 292,
  },
  {
    city: 'Perchtoldsdorf',
    postalZip: '17489',
    cvv: 456,
  },
  {
    city: 'Vadsø',
    postalZip: '1345 YC',
    cvv: 988,
  },
  {
    city: 'Hebei',
    postalZip: '47182',
    cvv: 268,
  },
  {
    city: 'Celaya',
    postalZip: '432468',
    cvv: 534,
  },
  {
    city: 'Çermik',
    postalZip: '967769',
    cvv: 962,
  },
  {
    city: 'Nelspruit',
    postalZip: '41-34',
    cvv: 892,
  },
  {
    city: 'Cork',
    postalZip: '552435',
    cvv: 775,
  },
  {
    city: 'Torghar',
    postalZip: '11860',
    cvv: 652,
  },
  {
    city: 'Bischofshofen',
    postalZip: '20308',
    cvv: 549,
  },
  {
    city: 'Malaybalay',
    postalZip: '766027',
    cvv: 822,
  },
  {
    city: 'Goiânia',
    postalZip: '4271',
    cvv: 368,
  },
  {
    city: 'Thiaumont',
    postalZip: '863334',
    cvv: 735,
  },
  {
    city: 'Novena',
    postalZip: '42060',
    cvv: 688,
  },
  {
    city: 'Skien',
    postalZip: '2591 UE',
    cvv: 313,
  },
  {
    city: 'Rijkevorsel',
    postalZip: '7304',
    cvv: 462,
  },
  {
    city: 'Gävle',
    postalZip: '227986',
    cvv: 460,
  },
  {
    city: 'Gorontalo',
    postalZip: '249744',
    cvv: 222,
  },
  {
    city: 'Finspång',
    postalZip: '2291-0082',
    cvv: 220,
  },
  {
    city: 'Paya Lebar',
    postalZip: '273164',
    cvv: 858,
  },
  {
    city: 'Langesund',
    postalZip: '07257',
    cvv: 653,
  },
  {
    city: 'Ödemiş',
    postalZip: '41414',
    cvv: 377,
  },
  {
    city: 'Uitenhage',
    postalZip: '3622',
    cvv: 290,
  },
  {
    city: 'Port Harcourt',
    postalZip: '61512',
    cvv: 135,
  },
  {
    city: 'Bontang',
    postalZip: '40565',
    cvv: 266,
  },
  {
    city: 'Tocopilla',
    postalZip: '36918',
    cvv: 582,
  },
  {
    city: 'Hamburg',
    postalZip: '63-535',
    cvv: 684,
  },
  {
    city: 'Kaliningrad',
    postalZip: '6374 IP',
    cvv: 172,
  },
  {
    city: 'Palopo',
    postalZip: '13739',
    cvv: 126,
  },
  {
    city: 'Mödling',
    postalZip: '5554',
    cvv: 545,
  },
  {
    city: 'Anklam',
    postalZip: '361384',
    cvv: 363,
  },
  {
    city: 'San Jose',
    postalZip: '26741',
    cvv: 576,
  },
  {
    city: 'Białystok',
    postalZip: '9882',
    cvv: 232,
  },
  {
    city: 'Dublin',
    postalZip: '447798',
    cvv: 322,
  },
  {
    city: 'St. Neots',
    postalZip: 'X7W 6JE',
    cvv: 837,
  },
  {
    city: 'Bischofshofen',
    postalZip: '29497',
    cvv: 159,
  },
  {
    city: 'Ollagüe',
    postalZip: '1355',
    cvv: 867,
  },
  {
    city: 'Mataram',
    postalZip: 'Q1 2QB',
    cvv: 672,
  },
  {
    city: 'Førde',
    postalZip: '7661-2316',
    cvv: 474,
  },
  {
    city: 'Queenstown',
    postalZip: '745419',
    cvv: 258,
  },
  {
    city: 'Yogyakarta',
    postalZip: '002362',
    cvv: 585,
  },
  {
    city: 'Nasirabad',
    postalZip: 'Y8C 1H5',
    cvv: 406,
  },
  {
    city: 'Pamplona',
    postalZip: '80064',
    cvv: 154,
  },
  {
    city: 'Piła',
    postalZip: '64421',
    cvv: 878,
  },
  {
    city: 'Villahermosa',
    postalZip: '2475',
    cvv: 539,
  },
  {
    city: 'Vigo',
    postalZip: '7305',
    cvv: 914,
  },
  {
    city: 'Ashburton',
    postalZip: '816413',
    cvv: 941,
  },
  {
    city: 'Burnpur',
    postalZip: '44007',
    cvv: 619,
  },
  {
    city: 'Jiangsu',
    postalZip: '12715',
    cvv: 340,
  },
  {
    city: 'Seogwipo',
    postalZip: '54373-143',
    cvv: 677,
  },
  {
    city: 'Kano',
    postalZip: '05415',
    cvv: 683,
  },
  {
    city: 'Oordegem',
    postalZip: '73891',
    cvv: 123,
  },
  {
    city: 'Passi',
    postalZip: 'E58 9PV',
    cvv: 438,
  },
  {
    city: 'Dublin',
    postalZip: '04583',
    cvv: 275,
  },
  {
    city: 'Whitehorse',
    postalZip: '74941',
    cvv: 771,
  },
  {
    city: 'Tomaszów Mazowiecki',
    postalZip: '429211',
    cvv: 782,
  },
  {
    city: 'Macau',
    postalZip: '3773',
    cvv: 821,
  },
  {
    city: 'Mejillones',
    postalZip: '2853',
    cvv: 564,
  },
  {
    city: 'Flin Flon',
    postalZip: '7175',
    cvv: 708,
  },
  {
    city: 'Puntarenas',
    postalZip: '48759',
    cvv: 356,
  },
  {
    city: 'Pukekohe',
    postalZip: '181158',
    cvv: 146,
  },
  {
    city: 'Alta',
    postalZip: '555178',
    cvv: 844,
  },
  {
    city: 'Mokpo',
    postalZip: '30703',
    cvv: 419,
  },
  {
    city: 'Bekasi',
    postalZip: '19161',
    cvv: 352,
  },
  {
    city: 'Motala',
    postalZip: '9777 HC',
    cvv: 428,
  },
  {
    city: 'Vị Thanh',
    postalZip: '69463',
    cvv: 870,
  },
  {
    city: 'Rendsburg',
    postalZip: '234693',
    cvv: 618,
  },
  {
    city: 'Motala',
    postalZip: '756744',
    cvv: 344,
  },
  {
    city: 'Gangneung',
    postalZip: '2729',
    cvv: 643,
  },
  {
    city: 'Cauayan',
    postalZip: '25604-53279',
    cvv: 310,
  },
  {
    city: 'Upplands Väsby',
    postalZip: '7581 VH',
    cvv: 985,
  },
  {
    city: 'Bandung',
    postalZip: '2811 NH',
    cvv: 708,
  },
  {
    city: 'Crato',
    postalZip: '84162',
    cvv: 503,
  },
  {
    city: 'Leersum',
    postalZip: '386000',
    cvv: 321,
  },
  {
    city: 'Bajaur Agency',
    postalZip: '62663',
    cvv: 687,
  },
  {
    city: 'Rocky Mountain House',
    postalZip: '38-42',
    cvv: 432,
  },
  {
    city: 'Tuyên Quang',
    postalZip: '23470',
    cvv: 220,
  },
  {
    city: 'Bangalore',
    postalZip: '68948',
    cvv: 150,
  },
  {
    city: 'Mora',
    postalZip: '664832',
    cvv: 737,
  },
  {
    city: 'Villa del Rosario',
    postalZip: '305997',
    cvv: 860,
  },
  {
    city: 'Mitú',
    postalZip: '94684',
    cvv: 779,
  },
  {
    city: 'Nowshera',
    postalZip: '711212',
    cvv: 839,
  },
  {
    city: 'Canberra',
    postalZip: '8202',
    cvv: 642,
  },
  {
    city: 'Bristol',
    postalZip: '713559',
    cvv: 684,
  },
  {
    city: 'Emmen',
    postalZip: '4551',
    cvv: 829,
  },
  {
    city: 'Fundación',
    postalZip: '594351',
    cvv: 895,
  },
  {
    city: 'Whakatane',
    postalZip: '64572',
    cvv: 849,
  },
  {
    city: 'Völkermarkt',
    postalZip: '25545',
    cvv: 553,
  },
  {
    city: 'Invercargill',
    postalZip: '24495',
    cvv: 192,
  },
  {
    city: 'Stavoren',
    postalZip: '7163',
    cvv: 678,
  },
  {
    city: 'Erlangen',
    postalZip: '288167',
    cvv: 359,
  },
  {
    city: 'Palma de Mallorca',
    postalZip: '24-26',
    cvv: 647,
  },
  {
    city: 'Central Water Catchment',
    postalZip: '2384',
    cvv: 326,
  },
  {
    city: 'Vienna',
    postalZip: '566586',
    cvv: 963,
  },
  {
    city: 'Gore',
    postalZip: '82-35',
    cvv: 787,
  },
  {
    city: 'Winterswijk',
    postalZip: '689602',
    cvv: 625,
  },
  {
    city: 'Boryeong',
    postalZip: '75798',
    cvv: 648,
  },
  {
    city: 'Khyber Agency',
    postalZip: '349560',
    cvv: 526,
  },
  {
    city: 'Armidale',
    postalZip: '604821',
    cvv: 667,
  },
  {
    city: 'Kaneohe',
    postalZip: '05936',
    cvv: 506,
  },
  {
    city: 'Tumaco',
    postalZip: '50216',
    cvv: 150,
  },
  {
    city: 'Zaria',
    postalZip: '266258',
    cvv: 162,
  },
  {
    city: 'Nampa',
    postalZip: '71671',
    cvv: 522,
  },
  {
    city: 'Neustrelitz',
    postalZip: '30427',
    cvv: 802,
  },
  {
    city: 'Dagupan City',
    postalZip: '3904',
    cvv: 857,
  },
  {
    city: 'Dublin',
    postalZip: '7489 PX',
    cvv: 433,
  },
  {
    city: 'Belford Roxo',
    postalZip: '29137',
    cvv: 861,
  },
  {
    city: 'Glovertown',
    postalZip: '280571',
    cvv: 869,
  },
  {
    city: 'Kavaratti',
    postalZip: '04447',
    cvv: 267,
  },
  {
    city: 'Almere',
    postalZip: '50113',
    cvv: 441,
  },
  {
    city: 'Dublin',
    postalZip: '8569-9073',
    cvv: 593,
  },
  {
    city: 'Bama',
    postalZip: '392820',
    cvv: 990,
  },
  {
    city: 'Melilla',
    postalZip: '677888',
    cvv: 143,
  },
  {
    city: 'Nha Trang',
    postalZip: '645844',
    cvv: 369,
  },
  {
    city: 'Wrocław',
    postalZip: '68322',
    cvv: 915,
  },
  {
    city: 'Balıkesir',
    postalZip: '24562',
    cvv: 201,
  },
  {
    city: 'Großpetersdorf',
    postalZip: '6152',
    cvv: 843,
  },
  {
    city: 'Yeosu',
    postalZip: '265673',
    cvv: 425,
  },
  {
    city: 'Iquitos',
    postalZip: 'S1T 3L4',
    cvv: 527,
  },
  {
    city: 'Agartala',
    postalZip: '392503',
    cvv: 343,
  },
  {
    city: 'Voronezh',
    postalZip: '50407',
    cvv: 280,
  },
  {
    city: 'Lagos',
    postalZip: '96947',
    cvv: 921,
  },
  {
    city: 'Monterrey',
    postalZip: '293047',
    cvv: 477,
  },
  {
    city: 'Hunstanton',
    postalZip: '16428',
    cvv: 663,
  },
  {
    city: 'Peshawar',
    postalZip: '22-93',
    cvv: 396,
  },
  {
    city: 'Angoulême',
    postalZip: '13977',
    cvv: 810,
  },
  {
    city: 'Pievepelago',
    postalZip: '23515',
    cvv: 129,
  },
  {
    city: 'Pamplona',
    postalZip: '1716',
    cvv: 754,
  },
  {
    city: 'Dera Bugti',
    postalZip: '2106',
    cvv: 743,
  },
  {
    city: 'San Antonio',
    postalZip: '21648-117',
    cvv: 501,
  },
  {
    city: 'Tranås',
    postalZip: '2276-4347',
    cvv: 517,
  },
  {
    city: 'Rawalakot',
    postalZip: '511072',
    cvv: 779,
  },
  {
    city: 'Tauranga',
    postalZip: '25735',
    cvv: 846,
  },
  {
    city: 'Palma de Mallorca',
    postalZip: '627044',
    cvv: 611,
  },
  {
    city: 'Randburg',
    postalZip: '13-863',
    cvv: 534,
  },
  {
    city: 'Forres',
    postalZip: '26-33',
    cvv: 564,
  },
  {
    city: 'Mykolaiv',
    postalZip: '27869-80393',
    cvv: 586,
  },
  {
    city: 'Chortkiv',
    postalZip: '16685',
    cvv: 339,
  },
  {
    city: 'Brest',
    postalZip: '6430',
    cvv: 435,
  },
  {
    city: 'Voronezh',
    postalZip: '4136',
    cvv: 242,
  },
  {
    city: 'Hollabrunn',
    postalZip: '20418',
    cvv: 824,
  },
  {
    city: 'Vienna',
    postalZip: '358502',
    cvv: 465,
  },
  {
    city: 'Taupo',
    postalZip: '4406',
    cvv: 971,
  },
  {
    city: 'Narvik',
    postalZip: '4454',
    cvv: 138,
  },
  {
    city: 'Pinetown',
    postalZip: '7931',
    cvv: 669,
  },
  {
    city: 'Belfast',
    postalZip: '300617',
    cvv: 676,
  },
  {
    city: 'Batangas City',
    postalZip: 'HS22 7XO',
    cvv: 911,
  },
  {
    city: 'Cagnes-sur-Mer',
    postalZip: '538205',
    cvv: 168,
  },
  {
    city: 'Lerum',
    postalZip: '6233',
    cvv: 929,
  },
  {
    city: 'Berdychiv',
    postalZip: '6686 GF',
    cvv: 918,
  },
  {
    city: 'Monteu Roero',
    postalZip: '1921-3486',
    cvv: 274,
  },
  {
    city: 'Essex',
    postalZip: '59-145',
    cvv: 407,
  },
  {
    city: 'Whyalla',
    postalZip: 'A3N 8V9',
    cvv: 471,
  },
  {
    city: 'Yurimaguas',
    postalZip: '232820',
    cvv: 870,
  },
  {
    city: 'Hervey Bay',
    postalZip: '35414',
    cvv: 401,
  },
  {
    city: 'Götzis',
    postalZip: '58681-671',
    cvv: 310,
  },
  {
    city: 'Lipetsk',
    postalZip: '2644',
    cvv: 622,
  },
  {
    city: 'Yurimaguas',
    postalZip: '431517',
    cvv: 527,
  },
  {
    city: 'Dublin',
    postalZip: '3908',
    cvv: 997,
  },
  {
    city: 'Lochgilphead',
    postalZip: '86-61',
    cvv: 189,
  },
  {
    city: 'North-Eastern Islands',
    postalZip: '5827',
    cvv: 276,
  },
  {
    city: 'Tula',
    postalZip: '2171',
    cvv: 242,
  },
  {
    city: 'Skardu',
    postalZip: '3323 LJ',
    cvv: 312,
  },
  {
    city: 'Moulins',
    postalZip: '941673',
    cvv: 271,
  },
  {
    city: 'Cao Lãnh',
    postalZip: '73098',
    cvv: 250,
  },
  {
    city: 'Odessa',
    postalZip: '75822',
    cvv: 257,
  },
  {
    city: 'Great Yarmouth',
    postalZip: '7736',
    cvv: 694,
  },
  {
    city: 'Borlänge',
    postalZip: '438111',
    cvv: 291,
  },
  {
    city: 'Hồ Chí Minh City',
    postalZip: '03696',
    cvv: 736,
  },
  {
    city: 'Kediri',
    postalZip: '28-518',
    cvv: 437,
  },
  {
    city: 'Gravelbourg',
    postalZip: '722892',
    cvv: 706,
  },
  {
    city: 'Granada',
    postalZip: '84485',
    cvv: 772,
  },
  {
    city: 'Empangeni',
    postalZip: '68697',
    cvv: 310,
  },
  {
    city: 'Cabuyao',
    postalZip: '11665',
    cvv: 576,
  },
  {
    city: 'Pskov',
    postalZip: 'UI63 6KA',
    cvv: 435,
  },
  {
    city: 'Bhagalpur',
    postalZip: '67059-736',
    cvv: 235,
  },
  {
    city: 'Leticia',
    postalZip: '970623',
    cvv: 904,
  },
  {
    city: 'Denbigh',
    postalZip: '5822',
    cvv: 518,
  },
  {
    city: 'Mogi das Cruzes',
    postalZip: '18395',
    cvv: 809,
  },
  {
    city: 'Samsun',
    postalZip: '26796',
    cvv: 516,
  },
  {
    city: 'Kirov',
    postalZip: '23690',
    cvv: 584,
  },
  {
    city: 'Berdychiv',
    postalZip: '57186',
    cvv: 935,
  },
  {
    city: 'Cao Lãnh',
    postalZip: '58736',
    cvv: 294,
  },
  {
    city: 'Diego de Almagro',
    postalZip: '642159',
    cvv: 992,
  },
  {
    city: 'Paita',
    postalZip: '57-685',
    cvv: 968,
  },
  {
    city: 'Okara',
    postalZip: '63074',
    cvv: 917,
  },
  {
    city: "O'Higgins",
    postalZip: '6116-1320',
    cvv: 756,
  },
  {
    city: 'Frederick',
    postalZip: '582671',
    cvv: 672,
  },
  {
    city: 'Vadsø',
    postalZip: '927067',
    cvv: 411,
  },
  {
    city: 'Casper',
    postalZip: '64236',
    cvv: 332,
  },
  {
    city: 'Tyumen',
    postalZip: '42-28',
    cvv: 118,
  },
  {
    city: 'St. Pölten',
    postalZip: '142478',
    cvv: 201,
  },
  {
    city: 'Banjarmasin',
    postalZip: '5769-5275',
    cvv: 233,
  },
  {
    city: 'Blumenau',
    postalZip: '21282',
    cvv: 701,
  },
  {
    city: 'Chongqing',
    postalZip: 'A5Z 7E2',
    cvv: 407,
  },
  {
    city: 'Yemanzhelinsk',
    postalZip: 'T7R 2T6',
    cvv: 657,
  },
  {
    city: 'Huesca',
    postalZip: '4229',
    cvv: 152,
  },
  {
    city: 'Lutterworth',
    postalZip: 'UB9 9BF',
    cvv: 606,
  },
  {
    city: 'Lang',
    postalZip: '2752',
    cvv: 309,
  },
  {
    city: 'Tver',
    postalZip: '5608',
    cvv: 695,
  },
  {
    city: 'Kaliningrad',
    postalZip: '8112-5560',
    cvv: 491,
  },
  {
    city: 'Heilongjiang',
    postalZip: '83-591',
    cvv: 500,
  },
  {
    city: 'Namsos',
    postalZip: '25375-34722',
    cvv: 615,
  },
  {
    city: 'Cascavel',
    postalZip: '67M 5B2',
    cvv: 675,
  },
  {
    city: 'Paarl',
    postalZip: '16628',
    cvv: 155,
  },
  {
    city: 'Bragança',
    postalZip: '9273 CU',
    cvv: 891,
  },
  {
    city: 'Augusta',
    postalZip: '545673',
    cvv: 895,
  },
  {
    city: 'Cheltenham',
    postalZip: '829426',
    cvv: 694,
  },
  {
    city: 'Barranca',
    postalZip: '883846',
    cvv: 149,
  },
  {
    city: 'Blackwood',
    postalZip: '666476',
    cvv: 226,
  },
  {
    city: 'Olivar',
    postalZip: '18978',
    cvv: 941,
  },
  {
    city: 'Orito',
    postalZip: '48710',
    cvv: 145,
  },
  {
    city: 'Belém',
    postalZip: '4461',
    cvv: 717,
  },
  {
    city: 'Stevenage',
    postalZip: '5415',
    cvv: 701,
  },
  {
    city: 'Starachowice',
    postalZip: '212481',
    cvv: 619,
  },
  {
    city: 'Boise',
    postalZip: '66J 7N2',
    cvv: 493,
  },
  {
    city: 'Jiangsu',
    postalZip: '45697-72428',
    cvv: 198,
  },
  {
    city: 'Salamanca',
    postalZip: '68-83',
    cvv: 486,
  },
  {
    city: 'Hindeloopen',
    postalZip: '15125-390',
    cvv: 185,
  },
  {
    city: 'Dehradun',
    postalZip: '1788 MM',
    cvv: 597,
  },
  {
    city: 'Bragança',
    postalZip: '8723',
    cvv: 647,
  },
  {
    city: 'Port Moody',
    postalZip: '227241',
    cvv: 220,
  },
  {
    city: 'Aguazul',
    postalZip: '4045-4533',
    cvv: 187,
  },
  {
    city: 'Zapopan',
    postalZip: '546731',
    cvv: 960,
  },
  {
    city: 'Gressoney-La-Trinitè',
    postalZip: '16908-99104',
    cvv: 352,
  },
  {
    city: 'Petit-Hallet',
    postalZip: '414315',
    cvv: 312,
  },
  {
    city: 'Montigny-lès-Metz',
    postalZip: '91182-34235',
    cvv: 446,
  },
  {
    city: 'Alajuela',
    postalZip: '102516',
    cvv: 131,
  },
  {
    city: 'Cork',
    postalZip: '669455',
    cvv: 830,
  },
  {
    city: 'Liaoning',
    postalZip: '62791',
    cvv: 795,
  },
  {
    city: 'Lipa',
    postalZip: 'BH47 8SP',
    cvv: 440,
  },
  {
    city: 'Penza',
    postalZip: '54288',
    cvv: 828,
  },
  {
    city: 'Huelva',
    postalZip: '46215',
    cvv: 451,
  },
  {
    city: 'Szczecin',
    postalZip: '34528',
    cvv: 899,
  },
  {
    city: 'Montbliart',
    postalZip: '23837',
    cvv: 943,
  },
  {
    city: 'Cork',
    postalZip: '62796-325',
    cvv: 469,
  },
  {
    city: 'Port Augusta',
    postalZip: '42744',
    cvv: 388,
  },
  {
    city: 'Imphal',
    postalZip: '952399',
    cvv: 557,
  },
  {
    city: 'Kızılcahamam',
    postalZip: '54263',
    cvv: 482,
  },
  {
    city: 'Tierra Amarilla',
    postalZip: '78483',
    cvv: 383,
  },
  {
    city: 'Hangu',
    postalZip: '27761',
    cvv: 992,
  },
  {
    city: 'Tanjay',
    postalZip: '168531',
    cvv: 980,
  },
  {
    city: 'Tonalá',
    postalZip: '223064',
    cvv: 882,
  },
  {
    city: 'Fürstenwalde',
    postalZip: '78821',
    cvv: 306,
  },
  {
    city: 'Sapele',
    postalZip: '68461',
    cvv: 498,
  },
  {
    city: 'Bergama',
    postalZip: '5423',
    cvv: 702,
  },
  {
    city: 'Colchane',
    postalZip: 'EA97 6SD',
    cvv: 176,
  },
  {
    city: 'Queenstown',
    postalZip: '60410',
    cvv: 661,
  },
  {
    city: 'Chatillon',
    postalZip: '7504',
    cvv: 439,
  },
  {
    city: 'Chongqing',
    postalZip: '84-73',
    cvv: 122,
  },
  {
    city: 'Battagram',
    postalZip: '174827',
    cvv: 214,
  },
  {
    city: 'Bolsward',
    postalZip: '307237',
    cvv: 190,
  },
  {
    city: 'Kirriemuir',
    postalZip: '81-225',
    cvv: 487,
  },
  {
    city: 'Dera Ghazi Khan',
    postalZip: '297568',
    cvv: 864,
  },
  {
    city: 'Parauapebas',
    postalZip: '55330',
    cvv: 979,
  },
  {
    city: 'Makassar',
    postalZip: '46721',
    cvv: 497,
  },
  {
    city: 'Baubau',
    postalZip: '8144-4863',
    cvv: 556,
  },
  {
    city: 'Narvik',
    postalZip: '653035',
    cvv: 575,
  },
  {
    city: 'Inner Mongolia',
    postalZip: '15-37',
    cvv: 690,
  },
  {
    city: 'Arendal',
    postalZip: 'B43 1CX',
    cvv: 925,
  },
  {
    city: 'Kano',
    postalZip: '81447',
    cvv: 516,
  },
  {
    city: 'Koppervik',
    postalZip: '120258',
    cvv: 795,
  },
  {
    city: 'Boston',
    postalZip: '57635-56482',
    cvv: 862,
  },
  {
    city: 'Førde',
    postalZip: '62888',
    cvv: 891,
  },
  {
    city: 'Parauapebas',
    postalZip: '35947-59310',
    cvv: 644,
  },
  {
    city: 'Chuncheon',
    postalZip: '86571',
    cvv: 957,
  },
  {
    city: 'Juárez',
    postalZip: '597265',
    cvv: 769,
  },
  {
    city: 'Kano',
    postalZip: '25616-85776',
    cvv: 986,
  },
  {
    city: 'Malbaie',
    postalZip: '3854 MI',
    cvv: 953,
  },
  {
    city: 'Orchard',
    postalZip: '3138',
    cvv: 806,
  },
  {
    city: 'Chuncheon',
    postalZip: '6856-7564',
    cvv: 272,
  },
  {
    city: 'Tân An',
    postalZip: '97-32',
    cvv: 582,
  },
  {
    city: 'Elbistan',
    postalZip: '6267',
    cvv: 880,
  },
  {
    city: 'Valéncia',
    postalZip: '34117866',
    cvv: 144,
  },
  {
    city: 'Cockburn',
    postalZip: '73945',
    cvv: 364,
  },
  {
    city: 'Phalaborwa',
    postalZip: '6888',
    cvv: 492,
  },
  {
    city: 'Berwick',
    postalZip: '25-67',
    cvv: 629,
  },
  {
    city: 'Chihuahua',
    postalZip: '4308 EP',
    cvv: 298,
  },
  {
    city: 'Ninh Bình',
    postalZip: '4762 RT',
    cvv: 702,
  },
  {
    city: 'Sorsogon City',
    postalZip: '21175',
    cvv: 322,
  },
  {
    city: 'Tranås',
    postalZip: '6919',
    cvv: 689,
  },
  {
    city: 'Gdynia',
    postalZip: '866168',
    cvv: 311,
  },
  {
    city: 'Izmail',
    postalZip: '8055',
    cvv: 483,
  },
  {
    city: 'Potchefstroom',
    postalZip: '30703',
    cvv: 332,
  },
  {
    city: 'Pachuca',
    postalZip: '8283',
    cvv: 261,
  },
  {
    city: 'Zhejiang',
    postalZip: '6065',
    cvv: 920,
  },
  {
    city: 'Kallang',
    postalZip: '4523',
    cvv: 204,
  },
  {
    city: 'Bilbo',
    postalZip: '71663',
    cvv: 611,
  },
  {
    city: 'Oslo',
    postalZip: '93452-098',
    cvv: 469,
  },
  {
    city: 'Bastia',
    postalZip: '249247',
    cvv: 502,
  },
  {
    city: 'Lleida',
    postalZip: '32-41',
    cvv: 387,
  },
  {
    city: 'Chuncheon',
    postalZip: '298582',
    cvv: 747,
  },
  {
    city: 'Uddevalla',
    postalZip: '32749',
    cvv: 400,
  },
  {
    city: 'North-Eastern Islands',
    postalZip: 'WQ5I 1IK',
    cvv: 558,
  },
  {
    city: 'Odessa',
    postalZip: '7661',
    cvv: 984,
  },
  {
    city: 'Bắc Giang',
    postalZip: '958843',
    cvv: 602,
  },
  {
    city: 'Bukit Panjang',
    postalZip: '66853',
    cvv: 947,
  },
  {
    city: 'Manokwari',
    postalZip: '31361',
    cvv: 655,
  },
  {
    city: 'Dir',
    postalZip: '4774',
    cvv: 243,
  },
  {
    city: 'Selkirk',
    postalZip: '317445',
    cvv: 988,
  },
  {
    city: 'Kailua',
    postalZip: '7279',
    cvv: 292,
  },
  {
    city: 'Perchtoldsdorf',
    postalZip: '17489',
    cvv: 456,
  },
  {
    city: 'Vadsø',
    postalZip: '1345 YC',
    cvv: 988,
  },
  {
    city: 'Hebei',
    postalZip: '47182',
    cvv: 268,
  },
  {
    city: 'Celaya',
    postalZip: '432468',
    cvv: 534,
  },
  {
    city: 'Çermik',
    postalZip: '967769',
    cvv: 962,
  },
  {
    city: 'Nelspruit',
    postalZip: '41-34',
    cvv: 892,
  },
  {
    city: 'Cork',
    postalZip: '552435',
    cvv: 775,
  },
  {
    city: 'Torghar',
    postalZip: '11860',
    cvv: 652,
  },
  {
    city: 'Bischofshofen',
    postalZip: '20308',
    cvv: 549,
  },
  {
    city: 'Malaybalay',
    postalZip: '766027',
    cvv: 822,
  },
  {
    city: 'Goiânia',
    postalZip: '4271',
    cvv: 368,
  },
  {
    city: 'Thiaumont',
    postalZip: '863334',
    cvv: 735,
  },
  {
    city: 'Novena',
    postalZip: '42060',
    cvv: 688,
  },
  {
    city: 'Skien',
    postalZip: '2591 UE',
    cvv: 313,
  },
  {
    city: 'Rijkevorsel',
    postalZip: '7304',
    cvv: 462,
  },
  {
    city: 'Gävle',
    postalZip: '227986',
    cvv: 460,
  },
  {
    city: 'Gorontalo',
    postalZip: '249744',
    cvv: 222,
  },
  {
    city: 'Finspång',
    postalZip: '2291-0082',
    cvv: 220,
  },
  {
    city: 'Paya Lebar',
    postalZip: '273164',
    cvv: 858,
  },
  {
    city: 'Langesund',
    postalZip: '07257',
    cvv: 653,
  },
  {
    city: 'Ödemiş',
    postalZip: '41414',
    cvv: 377,
  },
  {
    city: 'Uitenhage',
    postalZip: '3622',
    cvv: 290,
  },
  {
    city: 'Port Harcourt',
    postalZip: '61512',
    cvv: 135,
  },
  {
    city: 'Bontang',
    postalZip: '40565',
    cvv: 266,
  },
  {
    city: 'Tocopilla',
    postalZip: '36918',
    cvv: 582,
  },
  {
    city: 'Hamburg',
    postalZip: '63-535',
    cvv: 684,
  },
  {
    city: 'Kaliningrad',
    postalZip: '6374 IP',
    cvv: 172,
  },
  {
    city: 'Palopo',
    postalZip: '13739',
    cvv: 126,
  },
  {
    city: 'Mödling',
    postalZip: '5554',
    cvv: 545,
  },
  {
    city: 'Anklam',
    postalZip: '361384',
    cvv: 363,
  },
  {
    city: 'San Jose',
    postalZip: '26741',
    cvv: 576,
  },
  {
    city: 'Białystok',
    postalZip: '9882',
    cvv: 232,
  },
  {
    city: 'Dublin',
    postalZip: '447798',
    cvv: 322,
  },
  {
    city: 'St. Neots',
    postalZip: 'X7W 6JE',
    cvv: 837,
  },
  {
    city: 'Bischofshofen',
    postalZip: '29497',
    cvv: 159,
  },
  {
    city: 'Ollagüe',
    postalZip: '1355',
    cvv: 867,
  },
  {
    city: 'Mataram',
    postalZip: 'Q1 2QB',
    cvv: 672,
  },
  {
    city: 'Førde',
    postalZip: '7661-2316',
    cvv: 474,
  },
  {
    city: 'Queenstown',
    postalZip: '745419',
    cvv: 258,
  },
  {
    city: 'Yogyakarta',
    postalZip: '002362',
    cvv: 585,
  },
  {
    city: 'Nasirabad',
    postalZip: 'Y8C 1H5',
    cvv: 406,
  },
  {
    city: 'Pamplona',
    postalZip: '80064',
    cvv: 154,
  },
  {
    city: 'Piła',
    postalZip: '64421',
    cvv: 878,
  },
  {
    city: 'Villahermosa',
    postalZip: '2475',
    cvv: 539,
  },
  {
    city: 'Vigo',
    postalZip: '7305',
    cvv: 914,
  },
  {
    city: 'Ashburton',
    postalZip: '816413',
    cvv: 941,
  },
  {
    city: 'Burnpur',
    postalZip: '44007',
    cvv: 619,
  },
  {
    city: 'Jiangsu',
    postalZip: '12715',
    cvv: 340,
  },
  {
    city: 'Seogwipo',
    postalZip: '54373-143',
    cvv: 677,
  },
  {
    city: 'Kano',
    postalZip: '05415',
    cvv: 683,
  },
  {
    city: 'Oordegem',
    postalZip: '73891',
    cvv: 123,
  },
  {
    city: 'Passi',
    postalZip: 'E58 9PV',
    cvv: 438,
  },
  {
    city: 'Dublin',
    postalZip: '04583',
    cvv: 275,
  },
  {
    city: 'Whitehorse',
    postalZip: '74941',
    cvv: 771,
  },
  {
    city: 'Tomaszów Mazowiecki',
    postalZip: '429211',
    cvv: 782,
  },
  {
    city: 'Macau',
    postalZip: '3773',
    cvv: 821,
  },
  {
    city: 'Mejillones',
    postalZip: '2853',
    cvv: 564,
  },
  {
    city: 'Flin Flon',
    postalZip: '7175',
    cvv: 708,
  },
  {
    city: 'Puntarenas',
    postalZip: '48759',
    cvv: 356,
  },
  {
    city: 'Pukekohe',
    postalZip: '181158',
    cvv: 146,
  },
  {
    city: 'Alta',
    postalZip: '555178',
    cvv: 844,
  },
  {
    city: 'Mokpo',
    postalZip: '30703',
    cvv: 419,
  },
  {
    city: 'Bekasi',
    postalZip: '19161',
    cvv: 352,
  },
  {
    city: 'Motala',
    postalZip: '9777 HC',
    cvv: 428,
  },
  {
    city: 'Vị Thanh',
    postalZip: '69463',
    cvv: 870,
  },
  {
    city: 'Rendsburg',
    postalZip: '234693',
    cvv: 618,
  },
  {
    city: 'Motala',
    postalZip: '756744',
    cvv: 344,
  },
  {
    city: 'Gangneung',
    postalZip: '2729',
    cvv: 643,
  },
  {
    city: 'Cauayan',
    postalZip: '25604-53279',
    cvv: 310,
  },
  {
    city: 'Upplands Väsby',
    postalZip: '7581 VH',
    cvv: 985,
  },
  {
    city: 'Bandung',
    postalZip: '2811 NH',
    cvv: 708,
  },
  {
    city: 'Crato',
    postalZip: '84162',
    cvv: 503,
  },
  {
    city: 'Leersum',
    postalZip: '386000',
    cvv: 321,
  },
  {
    city: 'Bajaur Agency',
    postalZip: '62663',
    cvv: 687,
  },
  {
    city: 'Rocky Mountain House',
    postalZip: '38-42',
    cvv: 432,
  },
  {
    city: 'Tuyên Quang',
    postalZip: '23470',
    cvv: 220,
  },
  {
    city: 'Bangalore',
    postalZip: '68948',
    cvv: 150,
  },
  {
    city: 'Mora',
    postalZip: '664832',
    cvv: 737,
  },
  {
    city: 'Villa del Rosario',
    postalZip: '305997',
    cvv: 860,
  },
  {
    city: 'Mitú',
    postalZip: '94684',
    cvv: 779,
  },
  {
    city: 'Nowshera',
    postalZip: '711212',
    cvv: 839,
  },
  {
    city: 'Canberra',
    postalZip: '8202',
    cvv: 642,
  },
  {
    city: 'Bristol',
    postalZip: '713559',
    cvv: 684,
  },
  {
    city: 'Emmen',
    postalZip: '4551',
    cvv: 829,
  },
  {
    city: 'Fundación',
    postalZip: '594351',
    cvv: 895,
  },
  {
    city: 'Whakatane',
    postalZip: '64572',
    cvv: 849,
  },
  {
    city: 'Völkermarkt',
    postalZip: '25545',
    cvv: 553,
  },
  {
    city: 'Invercargill',
    postalZip: '24495',
    cvv: 192,
  },
  {
    city: 'Stavoren',
    postalZip: '7163',
    cvv: 678,
  },
  {
    city: 'Erlangen',
    postalZip: '288167',
    cvv: 359,
  },
  {
    city: 'Palma de Mallorca',
    postalZip: '24-26',
    cvv: 647,
  },
  {
    city: 'Central Water Catchment',
    postalZip: '2384',
    cvv: 326,
  },
  {
    city: 'Vienna',
    postalZip: '566586',
    cvv: 963,
  },
  {
    city: 'Gore',
    postalZip: '82-35',
    cvv: 787,
  },
  {
    city: 'Winterswijk',
    postalZip: '689602',
    cvv: 625,
  },
  {
    city: 'Boryeong',
    postalZip: '75798',
    cvv: 648,
  },
  {
    city: 'Khyber Agency',
    postalZip: '349560',
    cvv: 526,
  },
  {
    city: 'Armidale',
    postalZip: '604821',
    cvv: 667,
  },
  {
    city: 'Kaneohe',
    postalZip: '05936',
    cvv: 506,
  },
  {
    city: 'Tumaco',
    postalZip: '50216',
    cvv: 150,
  },
  {
    city: 'Zaria',
    postalZip: '266258',
    cvv: 162,
  },
  {
    city: 'Nampa',
    postalZip: '71671',
    cvv: 522,
  },
  {
    city: 'Neustrelitz',
    postalZip: '30427',
    cvv: 802,
  },
  {
    city: 'Dagupan City',
    postalZip: '3904',
    cvv: 857,
  },
  {
    city: 'Dublin',
    postalZip: '7489 PX',
    cvv: 433,
  },
  {
    city: 'Belford Roxo',
    postalZip: '29137',
    cvv: 861,
  },
  {
    city: 'Glovertown',
    postalZip: '280571',
    cvv: 869,
  },
  {
    city: 'Kavaratti',
    postalZip: '04447',
    cvv: 267,
  },
  {
    city: 'Almere',
    postalZip: '50113',
    cvv: 441,
  },
  {
    city: 'Dublin',
    postalZip: '8569-9073',
    cvv: 593,
  },
  {
    city: 'Bama',
    postalZip: '392820',
    cvv: 990,
  },
  {
    city: 'Melilla',
    postalZip: '677888',
    cvv: 143,
  },
  {
    city: 'Nha Trang',
    postalZip: '645844',
    cvv: 369,
  },
  {
    city: 'Wrocław',
    postalZip: '68322',
    cvv: 915,
  },
  {
    city: 'Balıkesir',
    postalZip: '24562',
    cvv: 201,
  },
  {
    city: 'Großpetersdorf',
    postalZip: '6152',
    cvv: 843,
  },
  {
    city: 'Yeosu',
    postalZip: '265673',
    cvv: 425,
  },
  {
    city: 'Iquitos',
    postalZip: 'S1T 3L4',
    cvv: 527,
  },
  {
    city: 'Agartala',
    postalZip: '392503',
    cvv: 343,
  },
  {
    city: 'Voronezh',
    postalZip: '50407',
    cvv: 280,
  },
  {
    city: 'Lagos',
    postalZip: '96947',
    cvv: 921,
  },
  {
    city: 'Monterrey',
    postalZip: '293047',
    cvv: 477,
  },
  {
    city: 'Hunstanton',
    postalZip: '16428',
    cvv: 663,
  },
  {
    city: 'Peshawar',
    postalZip: '22-93',
    cvv: 396,
  },
  {
    city: 'Angoulême',
    postalZip: '13977',
    cvv: 810,
  },
  {
    city: 'Pievepelago',
    postalZip: '23515',
    cvv: 129,
  },
  {
    city: 'Pamplona',
    postalZip: '1716',
    cvv: 754,
  },
  {
    city: 'Dera Bugti',
    postalZip: '2106',
    cvv: 743,
  },
  {
    city: 'San Antonio',
    postalZip: '21648-117',
    cvv: 501,
  },
  {
    city: 'Tranås',
    postalZip: '2276-4347',
    cvv: 517,
  },
  {
    city: 'Rawalakot',
    postalZip: '511072',
    cvv: 779,
  },
  {
    city: 'Tauranga',
    postalZip: '25735',
    cvv: 846,
  },
  {
    city: 'Palma de Mallorca',
    postalZip: '627044',
    cvv: 611,
  },
  {
    city: 'Randburg',
    postalZip: '13-863',
    cvv: 534,
  },
  {
    city: 'Forres',
    postalZip: '26-33',
    cvv: 564,
  },
  {
    city: 'Mykolaiv',
    postalZip: '27869-80393',
    cvv: 586,
  },
  {
    city: 'Chortkiv',
    postalZip: '16685',
    cvv: 339,
  },
  {
    city: 'Brest',
    postalZip: '6430',
    cvv: 435,
  },
  {
    city: 'Voronezh',
    postalZip: '4136',
    cvv: 242,
  },
  {
    city: 'Hollabrunn',
    postalZip: '20418',
    cvv: 824,
  },
  {
    city: 'Vienna',
    postalZip: '358502',
    cvv: 465,
  },
  {
    city: 'Taupo',
    postalZip: '4406',
    cvv: 971,
  },
  {
    city: 'Narvik',
    postalZip: '4454',
    cvv: 138,
  },
  {
    city: 'Pinetown',
    postalZip: '7931',
    cvv: 669,
  },
  {
    city: 'Belfast',
    postalZip: '300617',
    cvv: 676,
  },
  {
    city: 'Batangas City',
    postalZip: 'HS22 7XO',
    cvv: 911,
  },
  {
    city: 'Cagnes-sur-Mer',
    postalZip: '538205',
    cvv: 168,
  },
  {
    city: 'Lerum',
    postalZip: '6233',
    cvv: 929,
  },
  {
    city: 'Berdychiv',
    postalZip: '6686 GF',
    cvv: 918,
  },
  {
    city: 'Monteu Roero',
    postalZip: '1921-3486',
    cvv: 274,
  },
  {
    city: 'Essex',
    postalZip: '59-145',
    cvv: 407,
  },
  {
    city: 'Whyalla',
    postalZip: 'A3N 8V9',
    cvv: 471,
  },
  {
    city: 'Yurimaguas',
    postalZip: '232820',
    cvv: 870,
  },
  {
    city: 'Hervey Bay',
    postalZip: '35414',
    cvv: 401,
  },
  {
    city: 'Götzis',
    postalZip: '58681-671',
    cvv: 310,
  },
  {
    city: 'Lipetsk',
    postalZip: '2644',
    cvv: 622,
  },
  {
    city: 'Yurimaguas',
    postalZip: '431517',
    cvv: 527,
  },
  {
    city: 'Dublin',
    postalZip: '3908',
    cvv: 997,
  },
  {
    city: 'Lochgilphead',
    postalZip: '86-61',
    cvv: 189,
  },
  {
    city: 'North-Eastern Islands',
    postalZip: '5827',
    cvv: 276,
  },
  {
    city: 'Tula',
    postalZip: '2171',
    cvv: 242,
  },
  {
    city: 'Skardu',
    postalZip: '3323 LJ',
    cvv: 312,
  },
  {
    city: 'Moulins',
    postalZip: '941673',
    cvv: 271,
  },
  {
    city: 'Cao Lãnh',
    postalZip: '73098',
    cvv: 250,
  },
  {
    city: 'Odessa',
    postalZip: '75822',
    cvv: 257,
  },
  {
    city: 'Great Yarmouth',
    postalZip: '7736',
    cvv: 694,
  },
  {
    city: 'Borlänge',
    postalZip: '438111',
    cvv: 291,
  },
  {
    city: 'Hồ Chí Minh City',
    postalZip: '03696',
    cvv: 736,
  },
  {
    city: 'Kediri',
    postalZip: '28-518',
    cvv: 437,
  },
  {
    city: 'Gravelbourg',
    postalZip: '722892',
    cvv: 706,
  },
  {
    city: 'Granada',
    postalZip: '84485',
    cvv: 772,
  },
  {
    city: 'Empangeni',
    postalZip: '68697',
    cvv: 310,
  },
  {
    city: 'Cabuyao',
    postalZip: '11665',
    cvv: 576,
  },
  {
    city: 'Pskov',
    postalZip: 'UI63 6KA',
    cvv: 435,
  },
  {
    city: 'Bhagalpur',
    postalZip: '67059-736',
    cvv: 235,
  },
  {
    city: 'Leticia',
    postalZip: '970623',
    cvv: 904,
  },
  {
    city: 'Denbigh',
    postalZip: '5822',
    cvv: 518,
  },
  {
    city: 'Mogi das Cruzes',
    postalZip: '18395',
    cvv: 809,
  },
  {
    city: 'Samsun',
    postalZip: '26796',
    cvv: 516,
  },
  {
    city: 'Kirov',
    postalZip: '23690',
    cvv: 584,
  },
  {
    city: 'Berdychiv',
    postalZip: '57186',
    cvv: 935,
  },
  {
    city: 'Cao Lãnh',
    postalZip: '58736',
    cvv: 294,
  },
  {
    city: 'Diego de Almagro',
    postalZip: '642159',
    cvv: 992,
  },
  {
    city: 'Paita',
    postalZip: '57-685',
    cvv: 968,
  },
  {
    city: 'Okara',
    postalZip: '63074',
    cvv: 917,
  },
  {
    city: "O'Higgins",
    postalZip: '6116-1320',
    cvv: 756,
  },
  {
    city: 'Frederick',
    postalZip: '582671',
    cvv: 672,
  },
  {
    city: 'Vadsø',
    postalZip: '927067',
    cvv: 411,
  },
  {
    city: 'Casper',
    postalZip: '64236',
    cvv: 332,
  },
  {
    city: 'Tyumen',
    postalZip: '42-28',
    cvv: 118,
  },
  {
    city: 'St. Pölten',
    postalZip: '142478',
    cvv: 201,
  },
  {
    city: 'Banjarmasin',
    postalZip: '5769-5275',
    cvv: 233,
  },
  {
    city: 'Blumenau',
    postalZip: '21282',
    cvv: 701,
  },
  {
    city: 'Chongqing',
    postalZip: 'A5Z 7E2',
    cvv: 407,
  },
  {
    city: 'Yemanzhelinsk',
    postalZip: 'T7R 2T6',
    cvv: 657,
  },
  {
    city: 'Huesca',
    postalZip: '4229',
    cvv: 152,
  },
  {
    city: 'Lutterworth',
    postalZip: 'UB9 9BF',
    cvv: 606,
  },
  {
    city: 'Lang',
    postalZip: '2752',
    cvv: 309,
  },
  {
    city: 'Tver',
    postalZip: '5608',
    cvv: 695,
  },
  {
    city: 'Kaliningrad',
    postalZip: '8112-5560',
    cvv: 491,
  },
  {
    city: 'Heilongjiang',
    postalZip: '83-591',
    cvv: 500,
  },
  {
    city: 'Namsos',
    postalZip: '25375-34722',
    cvv: 615,
  },
  {
    city: 'Cascavel',
    postalZip: '67M 5B2',
    cvv: 675,
  },
  {
    city: 'Paarl',
    postalZip: '16628',
    cvv: 155,
  },
  {
    city: 'Bragança',
    postalZip: '9273 CU',
    cvv: 891,
  },
  {
    city: 'Augusta',
    postalZip: '545673',
    cvv: 895,
  },
  {
    city: 'Cheltenham',
    postalZip: '829426',
    cvv: 694,
  },
  {
    city: 'Barranca',
    postalZip: '883846',
    cvv: 149,
  },
  {
    city: 'Blackwood',
    postalZip: '666476',
    cvv: 226,
  },
  {
    city: 'Olivar',
    postalZip: '18978',
    cvv: 941,
  },
  {
    city: 'Orito',
    postalZip: '48710',
    cvv: 145,
  },
  {
    city: 'Belém',
    postalZip: '4461',
    cvv: 717,
  },
  {
    city: 'Stevenage',
    postalZip: '5415',
    cvv: 701,
  },
  {
    city: 'Starachowice',
    postalZip: '212481',
    cvv: 619,
  },
  {
    city: 'Boise',
    postalZip: '66J 7N2',
    cvv: 493,
  },
  {
    city: 'Jiangsu',
    postalZip: '45697-72428',
    cvv: 198,
  },
  {
    city: 'Salamanca',
    postalZip: '68-83',
    cvv: 486,
  },
  {
    city: 'Hindeloopen',
    postalZip: '15125-390',
    cvv: 185,
  },
  {
    city: 'Dehradun',
    postalZip: '1788 MM',
    cvv: 597,
  },
  {
    city: 'Bragança',
    postalZip: '8723',
    cvv: 647,
  },
  {
    city: 'Port Moody',
    postalZip: '227241',
    cvv: 220,
  },
  {
    city: 'Aguazul',
    postalZip: '4045-4533',
    cvv: 187,
  },
  {
    city: 'Zapopan',
    postalZip: '546731',
    cvv: 960,
  },
  {
    city: 'Gressoney-La-Trinitè',
    postalZip: '16908-99104',
    cvv: 352,
  },
  {
    city: 'Petit-Hallet',
    postalZip: '414315',
    cvv: 312,
  },
  {
    city: 'Montigny-lès-Metz',
    postalZip: '91182-34235',
    cvv: 446,
  },
  {
    city: 'Alajuela',
    postalZip: '102516',
    cvv: 131,
  },
  {
    city: 'Cork',
    postalZip: '669455',
    cvv: 830,
  },
  {
    city: 'Liaoning',
    postalZip: '62791',
    cvv: 795,
  },
  {
    city: 'Lipa',
    postalZip: 'BH47 8SP',
    cvv: 440,
  },
  {
    city: 'Penza',
    postalZip: '54288',
    cvv: 828,
  },
  {
    city: 'Huelva',
    postalZip: '46215',
    cvv: 451,
  },
  {
    city: 'Szczecin',
    postalZip: '34528',
    cvv: 899,
  },
  {
    city: 'Montbliart',
    postalZip: '23837',
    cvv: 943,
  },
  {
    city: 'Cork',
    postalZip: '62796-325',
    cvv: 469,
  },
  {
    city: 'Port Augusta',
    postalZip: '42744',
    cvv: 388,
  },
  {
    city: 'Imphal',
    postalZip: '952399',
    cvv: 557,
  },
  {
    city: 'Kızılcahamam',
    postalZip: '54263',
    cvv: 482,
  },
  {
    city: 'Tierra Amarilla',
    postalZip: '78483',
    cvv: 383,
  },
  {
    city: 'Hangu',
    postalZip: '27761',
    cvv: 992,
  },
  {
    city: 'Tanjay',
    postalZip: '168531',
    cvv: 980,
  },
  {
    city: 'Tonalá',
    postalZip: '223064',
    cvv: 882,
  },
  {
    city: 'Fürstenwalde',
    postalZip: '78821',
    cvv: 306,
  },
  {
    city: 'Sapele',
    postalZip: '68461',
    cvv: 498,
  },
  {
    city: 'Bergama',
    postalZip: '5423',
    cvv: 702,
  },
]);
</script>
