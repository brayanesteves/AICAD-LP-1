<template>
    <div class="contacto-cards wrapper" id="formUniversityGeneral">					
        <p id="texto_selecciona" class="c u-padding-top-md u-padding-bottom-sm u-margin-bottom-null u-font-md"><span class="u-bold u-padding-left-lg u-font-lg">¿Tienes dudas? </span> Selecciona el campus con el que te gustaría contactar:<a name=”contacto” id="contacto">&nbsp;</a></p>
			<div class="card-content">
			    <article class="c-card-contact" v-for="contacto in contactos" :key="contacto">
					<div class="c-card-contact__img">
						<p>{{ contacto.pais }}</p>
						<img v-bind:src="contacto.imagenes" v-bind:alt="contacto.alt">
							<div class="c-card-contact__icon">
							<svg version="1.1" width="25px" height="25px" viewBox="0 0 40 40" enable-background="new 0 0 40 40" xml:space="preserve">
							    <g>
								<path d="M36.428,35.814c0.898,0,1.676-0.297,2.34-0.881L27.436,23.602c-0.271,0.192-0.535,0.383-0.783,0.563
										c-0.85,0.627-1.536,1.113-2.065,1.464c-0.526,0.351-1.229,0.705-2.106,1.071c-0.879,0.365-1.699,0.547-2.458,0.547H20h-0.022
										c-0.759,0-1.578-0.182-2.456-0.547c-0.878-0.366-1.581-0.723-2.107-1.071c-0.53-0.351-1.217-0.837-2.066-1.464
										c-0.236-0.173-0.499-0.363-0.782-0.564L1.23,34.934c0.664,0.586,1.442,0.881,2.341,0.881H36.428L36.428,35.814z"/>
								<path d="M2.255,16.464C1.407,15.898,0.655,15.25,0,14.521v17.241l9.989-9.988
										C7.991,20.38,5.415,18.61,2.255,16.464z"/>
								<path d="M37.766,16.464c-3.039,2.057-5.623,3.828-7.752,5.313l9.984,9.984V14.521
										C39.357,15.237,38.615,15.884,37.766,16.464z"/>
								<path d="M36.428,4.389H3.571c-1.146,0-2.027,0.387-2.645,1.16C0.309,6.323,0,7.29,0,8.451
										c0,0.938,0.41,1.952,1.229,3.046c0.818,1.094,1.688,1.952,2.611,2.579c0.506,0.357,2.031,1.417,4.575,3.18
										c1.375,0.951,2.569,1.783,3.595,2.5c0.875,0.607,1.63,1.137,2.252,1.573c0.072,0.053,0.185,0.133,0.334,0.239
										c0.161,0.113,0.364,0.261,0.616,0.442c0.483,0.349,0.885,0.634,1.205,0.849c0.32,0.217,0.706,0.459,1.162,0.727
										c0.453,0.268,0.881,0.471,1.283,0.602c0.402,0.135,0.774,0.201,1.116,0.201H20h0.021c0.342,0,0.715-0.066,1.12-0.201
										c0.397-0.131,0.827-0.334,1.28-0.602c0.455-0.268,0.843-0.51,1.16-0.727c0.321-0.215,0.722-0.5,1.207-0.849
										c0.248-0.183,0.453-0.329,0.612-0.44c0.15-0.108,0.265-0.188,0.336-0.241c0.484-0.336,1.24-0.86,2.259-1.568
										c1.851-1.287,4.575-3.178,8.187-5.684c1.088-0.76,1.996-1.675,2.725-2.747c0.729-1.069,1.092-2.194,1.092-3.369
										c0-0.982-0.354-1.823-1.059-2.522C38.232,4.737,37.395,4.389,36.428,4.389z"/>
							</g>
						</svg>
					</div>
				</div>
				<div class="c-card-contact__data">
					<p class="u-text-center u-bold" v-bind:id="contacto.id">{{contacto.nombre}}</p>
					<p class="u-text-center">{{contacto.Rol}}</p>
					<a v-bind:href="contacto.href" class="u-text-center u-bold u-block u-color-grado">{{contacto.tel}}</a>
				</div>
			</article>
		</div>
	</div>
</template>

<script>
export default {
    name: 'section4',
    props: ['contacto'],
    data() {
        return {
            contactos: [
                {
                    pais: 'Madrid',
                    imagenes: '../imagenes/mobile/university/becas-ayudas/contacto-campus-madrid.jpg',                    
                    id:'n01',
                    nombre: 'Celia Montoya',
                    alt: this.nombre,
                    Rol: 'Departamento de admisiones',
                    codigo:'+34',
                    tel:'914524167',
                    href: 'tel:'+'+34914524167',
                },
                {
                    pais: 'Málaga',
                    imagenes: '../imagenes/mobile/university/becas-ayudas/contacto-campus-malaga.png',                    
                    id:'n02',
                    nombre: 'Cristina Porras',
                    alt: this.nombre,
                    Rol: 'Responsable de admisiones',
                    codigo:'+34',
                    tel:'952 02 03 69',
                    href: 'tel:'+'+34'+'952020369',
                },
                {
                    pais: 'Valencia',
                    imagenes: '../imagenes/mobile/university/becas-ayudas/contacto-campus-valencia.png',                    
                    id:'n03',
                    nombre: 'Sefa Gómez',
                    alt: this.nombre,
                    Rol: 'Responsable de admisiones',
                    codigo:'+34',
                    tel:'96 339 02 32',
                    href: 'tel:'+'+34'+'963390232',
                },
                {
                    pais: 'Barcelona',
                    imagenes: '../imagenes/mobile/university/becas-ayudas/contacto-campus-barcelona.png',                    
                    id:'n04',
                    nombre: 'Cristina Borreguero',
                    alt: this.nombre,
                    Rol: 'Departamento de admisiones',
                    codigo:'+34',
                    tel:'93 414 44 44',
                    href: 'tel:'+'+34'+'934144444',
                },
                {
                    pais: 'Navarra',
                    imagenes: '../imagenes/mobile/university/becas-ayudas/contacto-campus-navarra2.png',                    
                    id:'n05',
                    nombre: 'Gonzalo Imázcoz',
                    alt: this.nombre,
                    Rol: 'Responsable de admisiones',
                    codigo:'+34',
                    tel:'948 29 01 55',
                    href: 'tel:'+'+34'+'948290155',
                },
                {
                    pais: 'Sevilla',
                    imagenes: '../imagenes/mobile/university/becas-ayudas/contacto-campus-sevilla.png',                    
                    id:'n06',
                    nombre: 'María Espinosa',
                    alt: this.nombre,
                    Rol: 'Coordinadora área universitaria',
                    codigo:'+34',
                    tel:'954 460 003',
                    href: 'tel:'+'+34'+'954460003',
                },
                {
                    pais: 'Zaragoza',
                    imagenes: '../imagenes/mobile/university/becas-ayudas/contacto-campus-zaragoza.jpg',                    
                    id:'n07',
                    nombre: 'Javier González',
                    alt: this.nombre,
                    Rol: 'Director Comercial',
                    codigo:'+34',
                    tel:'662 322 374',
                    href: 'tel:'+'+34'+'662322374',
                },
                {
                    pais: 'Granada',
                    imagenes: '../imagenes/mobile/university/becas-ayudas/contacto-campus-granada.png',                    
                    id:'n08',
                    nombre: 'Luis Liñán',
                    alt: this.nombre,
                    Rol: 'Departamento de admisiones',
                    codigo:'+34',
                    tel:'958 22 29 14',
                    href: 'tel:'+'+34'+'958222914',
                },
                
            ]
        }
    }
}
</script>