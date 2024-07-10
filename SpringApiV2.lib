// SPRING API V2

var plr = mc.thePlayer;
var world = mc.theWorld
var timer = mc.timer;

function setSpeed(Speed, Strafing)
{
    plr.motionX *= (Speed)
    plr.motionZ *= (Speed)
    if (Strafing) plr.onGround = true
}

function sendNewPacket(Packet)
{
    plr.sendQueue.addToSendQueue(new Packet)
}

function setPlayerPosition(PositionX, PositionY, PositionZ)
{
    plr.setPosition(PositionX, PositionY, PositionZ)
}

function displayMessage(Message, IsDebug)
{
    if (IsDebug) {
        Chat.print("[Debug]" + Message)
     } else Chat.print(Message)
}

function onLiquid() {
	if(world.getBlockState(new BlockPos(plr.posX, plr.posY - 1, plr.posZ)).getBlock().getMaterial().isLiquid()) {
	    return true
	}
	return false
}

var client = "net.minecraft.network.play.client"

var Packets = [
    C0FPacketConfirmTransaction = Java.type(client + ".C0FPacketConfirmTransaction"),
    C04PacketPlayerPosition = Java.type(client + ".C03PacketPlayer.C04PacketPlayerPosition"),
    C05PacketPlayerLook = Java.type(client + ".C03PacketPlayer.C05PacketPlayerLook"),
    C06PacketPlayerPosLook = Java.type(client + ".C03PacketPlayer.C06PacketPlayerPosLook"),
    C18PacketSpectate = Java.type(client + ".C18PacketSpectate"),
    C03PacketPlayer = Java.type(client + ".C03PacketPlayer"),
    C02PacketUseEntity = Java.type(client + ".C02PacketUseEntity"),
    C00PacketKeepAlive = Java.type(client + ".C00PacketKeepAlive"),
    C13PacketPlayerAbilities = Java.type(client + ".C13PacketPlayerAbilities"),
    C09PacketHeldItemChange = Java.type(client + ".C09PacketHeldItemChange"),
    C17PacketCustomPayload = Java.type(client + ".C17PacketCustomPayload"),
    C0CPacketInput = Java.type(client + ".C0CPacketInput"),
    C16PacketClientStatus = Java.type(client + ".C16PacketClientStatus"),
    C08PacketPlayerBlockPlacement = Java.type(client + ".C08PacketPlayerBlockPlacement"),
    C0EPacketClickWindow = Java.type(client + ".C0EPacketClickWindow"),
    ItemStack = Java.type("net.minecraft.item.ItemStack"),
    BlockPos = Java.type("net.minecraft.util.BlockPos"),
    Vec3 = Java.type("net.minecraft.util.Vec3"),
    Item = Java.type("net.minecraft.item.Item"),
    S12PacketEntityVelocity = Java.type('net.minecraft.network.play.server.S12PacketEntityVelocity'),
    S18PacketEntityTeleport = Java.type("net.minecraft.network.play.server.S18PacketEntityTeleport"),
    C0BPacketEntityAction = Java.type("net.minecraft.network.play.client.C0BPacketEntityAction"),
]
