<script>
  import { Canvas } from '@threlte/core'
  import Model from './components/Model.svelte'
  import {
		AmbientLight,
		OrbitControls,
		PerspectiveCamera,
    DirectionalLight
	} from '@threlte/core'
</script>

<div class="canvas-wrapper">

  <Canvas>
    <PerspectiveCamera fov={60} position={{ x: 0, y:0, z: 5 }}>
      <OrbitControls />
    </PerspectiveCamera>

    <DirectionalLight shadow intensity={5} position={{ x: 3, y: 2, z: 3 }} target={{ x: 1, y: 1, z: 1 }} />
    <Model />
  </Canvas>

</div>


<style>
  .canvas-wrapper {
    position: fixed;
	  top: 0;
	  left: 0;
	  width: 100%;
	  height: 100%;
  }
</style>