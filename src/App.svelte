<script>
  import { Canvas } from '@threlte/core'
  import Model from './components/Model.svelte'
  import {
		AmbientLight,
		OrbitControls,
		PerspectiveCamera
	} from '@threlte/core'
</script>

<div class="canvas-wrapper">

  <Canvas>
    <PerspectiveCamera fov={90} position={{ x: 0, y:0, z: -12 }}>
      <OrbitControls />
    </PerspectiveCamera>
    <AmbientLight intensity={0.9}  />

    <AmbientLight />  
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