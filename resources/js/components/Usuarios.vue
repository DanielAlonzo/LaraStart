<template>
    <div class="container">
        <div class="row mt-5">
          <div class="col-md-12">
            <div class="card">
              <div class="card-header">
                <h3 class="card-title">Lista de Usuarios</h3>

                <div class="card-tools">
                  <button type="button" class="btn btn-success" data-toggle="modal" data-target="#NuevoUsuario">Nuevo 
                      <i class="fas fa-user-plus"></i>
                  </button>
                </div>


              </div>
              <!-- /.card-header -->
              <div class="card-body table-responsive p-0">
                <table class="table table-hover">
                  <thead>
                    <tr>
                      <th>Id</th>
                      <th>Usuario</th>
                      <th>Email</th>
                      <th>Tipo de Usuario</th>
                      <th>Opciones</th>
                      
                      
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td>183</td>
                      <td>John Doe</td>
                      <td>11-7-2014</td>
                      <td><span class="tag tag-success">Approved</span></td>
                      <td>
                          <a href="">
                              <i class="fa fa-edit"></i>
                          </a>
                          |
                          <a href="">
                              <i class="fa fa-trash red"></i>
                          </a>
                      </td>
                    </tr>
                   
                  </tbody>
                </table>
              </div>
              <!-- /.card-body -->
            </div>
            <!-- /.card -->
          </div>
        </div>


                Modal
            <div class="modal fade" id="NuevoUsuario" tabindex="-1" role="dialog" aria-labelledby="NuevoUsuarioLabel" aria-hidden="true">
            <div class="modal-dialog modal-dialog-centered" role="document">
                <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="NuevoUsuarioLabel">Agregar Nuevo Usuario</h5>
                    <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                    <span aria-hidden="true">&times;</span>
                    </button>
                </div>
                <div class="modal-body">
                    
                    <div class="form-group">
                    
                    <input v-model="form.name" type="text" name="name"
                    placeholder="Nombre"
                        class="form-control" :class="{ 'is-invalid': form.errors.has('name') }">
                    <has-error :form="form" field="name"></has-error>
                    </div>

                </div>
                <div class="modal-footer">
                    <button type="button" class="btn btn-danger" data-dismiss="modal">Cancelar</button>
                    <button type="button" class="btn btn-success">Guardar</button>
                </div>
                </div>
            </div>
            </div>

    </div>


    
</template>

<script>
    export default {
        // data() {
        //     return{
        //         form:new Form({
        //             name:'',
        //             email:'',
        //             password:'',
        //             tipousuario:'',
        //             photo:''
                    
        //         })
        //     }
        // },
        mounted() {
            console.log('Component mounted.')
        }
    }
</script>
